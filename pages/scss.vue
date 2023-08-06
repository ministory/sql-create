<template>
<main role="main">
  <div class="container-fluid py-5">
    <h2 class="tit-h2 mt-5 text-center">SQL Script 생성</h2>
    <div class="round-box">
      <div class='row'>
        <div class='col-sm-6'>
          <div class="tit-btn text-center">
              <h3 class="mb-0 mt-2">SQL 생성</h3>
          </div>
          <hr class="mb-3" />
          <div class="btn-group flex-fill mr-2">
              <select>
                  <option value="">DBMS</option>
                  <option value="ORACLE">ORACLE</option>
                  <option value="MySQL">MySQL</option>
                  <option value="MSSQL">MSSQL</option>
                  <option value="PostgreSQL">PostgreSQL</option>
              </select>
          </div>
          <hr class="mb-3" />
          <div class="position-relative input-comment">
            <textarea class="form-control" rows="13"></textarea>
          </div>
          <div class="btn-area text-center">
            <a class="btn btn-primary btn-lg" href="#">GENARATE</a>
          </div>
        </div>
        <div class='col-sm-4'>
          <div class="tit-btn text-center">
              <h3 class="mb-0 mt-2">SQL 생성 결과</h3>
              <a type="button" class="btn-copy" title="SQL복사"><img class="btn-copy-img" src="~/assets/image/copy.png" /></a>
          </div>
          <div class="group-box set d-flex align-items-center mt-3">
              <div class="group-tit-info">
                <button class="tag button">Open API</button>
                <p class="sql text-muted">select a.dept_cd, a.dept_nm, a.use_yn, a.sort_seq, b.user_id from tbl_dept a, tbl_user b where a.dept_cd = b.dept_cd and a.dept_cd = '01234' and a.use_yn = 'Y' order by a.sort_seq desc</p>
              </div>
              <div class="group-tit-info">
                <button class="tag button-select">BAS</button>
                <p class="sql text-muted">select a.dept_cd, a.dept_nm, a.use_yn, a.sort_seq, b.user_id from tbl_dept a, tbl_user b where a.dept_cd = b.dept_cd and a.dept_cd = '01234' and a.use_yn = 'Y' order by a.sort_seq desc</p>
              </div>
          </div>
        </div>
        <div class='col-sm-2 history-list'>
          <div class="sql-cont">
            <p class="text-muted history">
              select dept_cd, dept_nm, use_yn, sort_seq, reg_dt, reg_id from tbl_dept where dept_cd = '01234'
            </p>
            <div class="focus-active input-group-append-twin d-flex align-items-center justify-content-center">
              <em title="삭제" class="fas icon-input-del"></em>
            </div>
          </div>
          <div class="sql-cont">
            <p class="text-muted history">
              select a.dept_cd, a.dept_nm, a.use_yn, a.sort_seq, b.user_id from tbl_dept a, tbl_user b where a.dept_cd = b.dept_cd and a.dept_cd = '01234' and a.use_yn = 'Y' order by a.sort_seq desc
            </p>
            <div class="focus-active input-group-append-twin d-flex align-items-center justify-content-center">
              <em title="삭제" class="fas icon-input-del"></em>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</main>
</template>