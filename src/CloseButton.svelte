<style>
.closeAnnoucement {
    position: absolute;
    top: 0;
    right: 0;
    display: flex;
    align-items: center;
    justify-content: center;
}

.closeAnnoucement:after {
    content: '×';
    display: block;
    font-family: helvetica,arial,sans-serif;
    font-weight: normal;
    cursor: pointer;
}

span {
    background-color: rgba(0,0,0,.15);
    height: 100%;
    width: 3.5rem;
}

span:after {
    font-size: 1.7rem;
}
</style>


<span
    class="closeAnnoucement"
    tabIndex="0"
    role="button"
    aria-label="Close Announcement"
></span>