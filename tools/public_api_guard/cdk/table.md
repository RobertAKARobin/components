## API Report File for "components-srcs"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AfterContentChecked } from '@angular/core';
import { BehaviorSubject } from 'rxjs';
import { BooleanInput } from '@angular/cdk/coercion';
import { ChangeDetectorRef } from '@angular/core';
import { CollectionViewer } from '@angular/cdk/collections';
import { DataSource } from '@angular/cdk/collections';
import { Direction } from '@angular/cdk/bidi';
import { Directionality } from '@angular/cdk/bidi';
import { ElementRef } from '@angular/core';
import * as i0 from '@angular/core';
import * as i5 from '@angular/cdk/scrolling';
import { InjectionToken } from '@angular/core';
import { IterableChanges } from '@angular/core';
import { IterableDiffer } from '@angular/core';
import { IterableDiffers } from '@angular/core';
import { NgZone } from '@angular/core';
import { Observable } from 'rxjs';
import { OnChanges } from '@angular/core';
import { OnDestroy } from '@angular/core';
import { OnInit } from '@angular/core';
import { Platform } from '@angular/cdk/platform';
import { QueryList } from '@angular/core';
import { SimpleChanges } from '@angular/core';
import { TemplateRef } from '@angular/core';
import { TrackByFunction } from '@angular/core';
import { ViewContainerRef } from '@angular/core';
import { ViewportRuler } from '@angular/cdk/scrolling';
import { _ViewRepeater } from '@angular/cdk/collections';

// @public
export class BaseCdkCell {
    constructor(columnDef: CdkColumnDef, elementRef: ElementRef);
}

// @public
export abstract class BaseRowDef implements OnChanges {
    constructor(
    template: TemplateRef<any>, _differs: IterableDiffers);
    columns: Iterable<string>;
    protected _columnsDiffer: IterableDiffer<any>;
    // (undocumented)
    protected _differs: IterableDiffers;
    extractCellTemplate(column: CdkColumnDef): TemplateRef<any>;
    getColumnsDiff(): IterableChanges<any> | null;
    // (undocumented)
    ngOnChanges(changes: SimpleChanges): void;
    template: TemplateRef<any>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<BaseRowDef, never, never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<BaseRowDef, never>;
}

// @public
export interface CanStick {
    hasStickyChanged(): boolean;
    _hasStickyChanged: boolean;
    resetStickyChanged(): void;
    sticky: boolean;
}

// @public
export type CanStickCtor = Constructor<CanStick>;

// @public
export const CDK_ROW_TEMPLATE = "<ng-container cdkCellOutlet></ng-container>";

// @public
export const CDK_TABLE: InjectionToken<any>;

// @public
export const CDK_TABLE_TEMPLATE = "\n  <ng-content select=\"caption\"></ng-content>\n  <ng-content select=\"colgroup, col\"></ng-content>\n  <ng-container headerRowOutlet></ng-container>\n  <ng-container rowOutlet></ng-container>\n  <ng-container noDataRowOutlet></ng-container>\n  <ng-container footerRowOutlet></ng-container>\n";

// @public
export class CdkCell extends BaseCdkCell {
    constructor(columnDef: CdkColumnDef, elementRef: ElementRef);
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkCell, "cdk-cell, td[cdk-cell]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkCell, never>;
}

// @public
export class CdkCellDef implements CellDef {
    constructor(template: TemplateRef<any>);
    // (undocumented)
    template: TemplateRef<any>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkCellDef, "[cdkCellDef]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkCellDef, never>;
}

// @public
export class CdkCellOutlet implements OnDestroy {
    constructor(_viewContainer: ViewContainerRef);
    cells: CdkCellDef[];
    context: any;
    static mostRecentCellOutlet: CdkCellOutlet | null;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    _viewContainer: ViewContainerRef;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkCellOutlet, "[cdkCellOutlet]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkCellOutlet, never>;
}

// @public
export interface CdkCellOutletMultiRowContext<T> {
    $implicit?: T;
    count?: number;
    dataIndex?: number;
    even?: boolean;
    first?: boolean;
    last?: boolean;
    odd?: boolean;
    renderIndex?: number;
}

// @public
export interface CdkCellOutletRowContext<T> {
    $implicit?: T;
    count?: number;
    even?: boolean;
    first?: boolean;
    index?: number;
    last?: boolean;
    odd?: boolean;
}

// @public
export class CdkColumnDef extends _CdkColumnDefBase implements CanStick {
    constructor(_table?: any);
    cell: CdkCellDef;
    _columnCssClassName: string[];
    cssClassFriendlyName: string;
    footerCell: CdkFooterCellDef;
    headerCell: CdkHeaderCellDef;
    get name(): string;
    set name(name: string);
    // (undocumented)
    protected _name: string;
    // (undocumented)
    static ngAcceptInputType_sticky: BooleanInput;
    // (undocumented)
    static ngAcceptInputType_stickyEnd: BooleanInput;
    protected _setNameInput(value: string): void;
    get stickyEnd(): boolean;
    set stickyEnd(v: boolean);
    // (undocumented)
    _stickyEnd: boolean;
    // (undocumented)
    _table?: any;
    protected _updateColumnCssClassName(): void;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkColumnDef, "[cdkColumnDef]", never, { "sticky": "sticky"; "name": "cdkColumnDef"; "stickyEnd": "stickyEnd"; }, {}, ["cell", "headerCell", "footerCell"]>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkColumnDef, [{ optional: true; }]>;
}

// @public
export class CdkFooterCell extends BaseCdkCell {
    constructor(columnDef: CdkColumnDef, elementRef: ElementRef);
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkFooterCell, "cdk-footer-cell, td[cdk-footer-cell]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkFooterCell, never>;
}

// @public
export class CdkFooterCellDef implements CellDef {
    constructor(template: TemplateRef<any>);
    // (undocumented)
    template: TemplateRef<any>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkFooterCellDef, "[cdkFooterCellDef]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkFooterCellDef, never>;
}

// @public
export class CdkFooterRow {
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<CdkFooterRow, "cdk-footer-row, tr[cdk-footer-row]", never, {}, {}, never, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkFooterRow, never>;
}

// @public
export class CdkFooterRowDef extends _CdkFooterRowDefBase implements CanStick, OnChanges {
    constructor(template: TemplateRef<any>, _differs: IterableDiffers, _table?: any);
    // (undocumented)
    static ngAcceptInputType_sticky: BooleanInput;
    // (undocumented)
    ngOnChanges(changes: SimpleChanges): void;
    // (undocumented)
    _table?: any;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkFooterRowDef, "[cdkFooterRowDef]", never, { "columns": "cdkFooterRowDef"; "sticky": "cdkFooterRowDefSticky"; }, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkFooterRowDef, [null, null, { optional: true; }]>;
}

// @public
export class CdkHeaderCell extends BaseCdkCell {
    constructor(columnDef: CdkColumnDef, elementRef: ElementRef);
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkHeaderCell, "cdk-header-cell, th[cdk-header-cell]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkHeaderCell, never>;
}

// @public
export class CdkHeaderCellDef implements CellDef {
    constructor(template: TemplateRef<any>);
    // (undocumented)
    template: TemplateRef<any>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkHeaderCellDef, "[cdkHeaderCellDef]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkHeaderCellDef, never>;
}

// @public
export class CdkHeaderRow {
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<CdkHeaderRow, "cdk-header-row, tr[cdk-header-row]", never, {}, {}, never, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkHeaderRow, never>;
}

// @public
export class CdkHeaderRowDef extends _CdkHeaderRowDefBase implements CanStick, OnChanges {
    constructor(template: TemplateRef<any>, _differs: IterableDiffers, _table?: any);
    // (undocumented)
    static ngAcceptInputType_sticky: BooleanInput;
    // (undocumented)
    ngOnChanges(changes: SimpleChanges): void;
    // (undocumented)
    _table?: any;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkHeaderRowDef, "[cdkHeaderRowDef]", never, { "columns": "cdkHeaderRowDef"; "sticky": "cdkHeaderRowDefSticky"; }, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkHeaderRowDef, [null, null, { optional: true; }]>;
}

// @public
export class CdkNoDataRow {
    constructor(templateRef: TemplateRef<any>);
    // (undocumented)
    templateRef: TemplateRef<any>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkNoDataRow, "ng-template[cdkNoDataRow]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkNoDataRow, never>;
}

// @public
export class CdkRecycleRows {
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkRecycleRows, "cdk-table[recycleRows], table[cdk-table][recycleRows]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkRecycleRows, never>;
}

// @public
export class CdkRow {
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<CdkRow, "cdk-row, tr[cdk-row]", never, {}, {}, never, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkRow, never>;
}

// @public
export class CdkRowDef<T> extends BaseRowDef {
    constructor(template: TemplateRef<any>, _differs: IterableDiffers, _table?: any);
    // (undocumented)
    _table?: any;
    when: (index: number, rowData: T) => boolean;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkRowDef<any>, "[cdkRowDef]", never, { "columns": "cdkRowDefColumns"; "when": "cdkRowDefWhen"; }, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkRowDef<any>, [null, null, { optional: true; }]>;
}

// @public
export class CdkTable<T> implements AfterContentChecked, CollectionViewer, OnDestroy, OnInit {
    constructor(_differs: IterableDiffers, _changeDetectorRef: ChangeDetectorRef, _elementRef: ElementRef, role: string, _dir: Directionality, _document: any, _platform: Platform, _viewRepeater: _ViewRepeater<T, RenderRow<T>, RowContext<T>>, _coalescedStyleScheduler: _CoalescedStyleScheduler, _viewportRuler: ViewportRuler,
    _stickyPositioningListener: StickyPositioningListener);
    addColumnDef(columnDef: CdkColumnDef): void;
    addFooterRowDef(footerRowDef: CdkFooterRowDef): void;
    addHeaderRowDef(headerRowDef: CdkHeaderRowDef): void;
    addRowDef(rowDef: CdkRowDef<T>): void;
    // (undocumented)
    protected readonly _changeDetectorRef: ChangeDetectorRef;
    // (undocumented)
    protected readonly _coalescedStyleScheduler: _CoalescedStyleScheduler;
    _contentColumnDefs: QueryList<CdkColumnDef>;
    _contentFooterRowDefs: QueryList<CdkFooterRowDef>;
    _contentHeaderRowDefs: QueryList<CdkHeaderRowDef>;
    _contentRowDefs: QueryList<CdkRowDef<T>>;
    protected _data: readonly T[];
    get dataSource(): CdkTableDataSourceInput<T>;
    set dataSource(dataSource: CdkTableDataSourceInput<T>);
    // (undocumented)
    protected readonly _differs: IterableDiffers;
    // (undocumented)
    protected readonly _dir: Directionality;
    // (undocumented)
    protected readonly _elementRef: ElementRef;
    get fixedLayout(): boolean;
    set fixedLayout(v: boolean);
    // (undocumented)
    _footerRowOutlet: FooterRowOutlet;
    _getRenderedRows(rowOutlet: RowOutlet): HTMLElement[];
    _getRowDefs(data: T, dataIndex: number): CdkRowDef<T>[];
    // (undocumented)
    _headerRowOutlet: HeaderRowOutlet;
    protected _isNativeHtmlTable: boolean;
    get multiTemplateDataRows(): boolean;
    set multiTemplateDataRows(v: boolean);
    // (undocumented)
    _multiTemplateDataRows: boolean;
    protected needsPositionStickyOnElement: boolean;
    // (undocumented)
    static ngAcceptInputType_fixedLayout: BooleanInput;
    // (undocumented)
    static ngAcceptInputType_multiTemplateDataRows: BooleanInput;
    // (undocumented)
    ngAfterContentChecked(): void;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    ngOnInit(): void;
    _noDataRow: CdkNoDataRow;
    // (undocumented)
    _noDataRowOutlet: NoDataRowOutlet;
    removeColumnDef(columnDef: CdkColumnDef): void;
    removeFooterRowDef(footerRowDef: CdkFooterRowDef): void;
    removeHeaderRowDef(headerRowDef: CdkHeaderRowDef): void;
    removeRowDef(rowDef: CdkRowDef<T>): void;
    renderRows(): void;
    // (undocumented)
    _rowOutlet: DataRowOutlet;
    setNoDataRow(noDataRow: CdkNoDataRow | null): void;
    protected stickyCssClass: string;
    // @deprecated (undocumented)
    protected readonly _stickyPositioningListener: StickyPositioningListener;
    get trackBy(): TrackByFunction<T>;
    set trackBy(fn: TrackByFunction<T>);
    updateStickyColumnStyles(): void;
    updateStickyFooterRowStyles(): void;
    updateStickyHeaderRowStyles(): void;
    readonly viewChange: BehaviorSubject<{
        start: number;
        end: number;
    }>;
    // (undocumented)
    protected readonly _viewRepeater: _ViewRepeater<T, RenderRow<T>, RowContext<T>>;
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<CdkTable<any>, "cdk-table, table[cdk-table]", ["cdkTable"], { "trackBy": "trackBy"; "dataSource": "dataSource"; "multiTemplateDataRows": "multiTemplateDataRows"; "fixedLayout": "fixedLayout"; }, {}, ["_noDataRow", "_contentColumnDefs", "_contentRowDefs", "_contentHeaderRowDefs", "_contentFooterRowDefs"], ["caption", "colgroup, col"]>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkTable<any>, [null, null, null, { attribute: "role"; }, { optional: true; }, null, null, null, null, null, { optional: true; skipSelf: true; }]>;
}

// @public (undocumented)
export class CdkTableModule {
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkTableModule, never>;
    // (undocumented)
    static ɵinj: i0.ɵɵInjectorDeclaration<CdkTableModule>;
    // (undocumented)
    static ɵmod: i0.ɵɵNgModuleDeclaration<CdkTableModule, [typeof i1.CdkTable, typeof i2.CdkRowDef, typeof i3.CdkCellDef, typeof i2.CdkCellOutlet, typeof i3.CdkHeaderCellDef, typeof i3.CdkFooterCellDef, typeof i3.CdkColumnDef, typeof i3.CdkCell, typeof i2.CdkRow, typeof i3.CdkHeaderCell, typeof i3.CdkFooterCell, typeof i2.CdkHeaderRow, typeof i2.CdkHeaderRowDef, typeof i2.CdkFooterRow, typeof i2.CdkFooterRowDef, typeof i1.DataRowOutlet, typeof i1.HeaderRowOutlet, typeof i1.FooterRowOutlet, typeof i4.CdkTextColumn, typeof i2.CdkNoDataRow, typeof i1.CdkRecycleRows, typeof i1.NoDataRowOutlet], [typeof i5.ScrollingModule], [typeof i1.CdkTable, typeof i2.CdkRowDef, typeof i3.CdkCellDef, typeof i2.CdkCellOutlet, typeof i3.CdkHeaderCellDef, typeof i3.CdkFooterCellDef, typeof i3.CdkColumnDef, typeof i3.CdkCell, typeof i2.CdkRow, typeof i3.CdkHeaderCell, typeof i3.CdkFooterCell, typeof i2.CdkHeaderRow, typeof i2.CdkHeaderRowDef, typeof i2.CdkFooterRow, typeof i2.CdkFooterRowDef, typeof i1.DataRowOutlet, typeof i1.HeaderRowOutlet, typeof i1.FooterRowOutlet, typeof i4.CdkTextColumn, typeof i2.CdkNoDataRow, typeof i1.CdkRecycleRows, typeof i1.NoDataRowOutlet]>;
}

// @public
export class CdkTextColumn<T> implements OnDestroy, OnInit {
    constructor(_table: CdkTable<T>, _options: TextColumnOptions<T>);
    cell: CdkCellDef;
    columnDef: CdkColumnDef;
    _createDefaultHeaderText(): string;
    dataAccessor: (data: T, name: string) => string;
    headerCell: CdkHeaderCellDef;
    headerText: string;
    justify: 'start' | 'end';
    get name(): string;
    set name(name: string);
    // (undocumented)
    _name: string;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    ngOnInit(): void;
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<CdkTextColumn<any>, "cdk-text-column", never, { "name": "name"; "headerText": "headerText"; "dataAccessor": "dataAccessor"; "justify": "justify"; }, {}, never, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkTextColumn<any>, [{ optional: true; }, { optional: true; }]>;
}

// @public
export interface CellDef {
    // (undocumented)
    template: TemplateRef<any>;
}

// @public
export const _COALESCED_STYLE_SCHEDULER: InjectionToken<_CoalescedStyleScheduler>;

// @public
export class _CoalescedStyleScheduler implements OnDestroy {
    constructor(_ngZone: NgZone);
    ngOnDestroy(): void;
    schedule(task: () => unknown): void;
    scheduleEnd(task: () => unknown): void;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<_CoalescedStyleScheduler, never>;
    // (undocumented)
    static ɵprov: i0.ɵɵInjectableDeclaration<_CoalescedStyleScheduler>;
}

// @public
export type Constructor<T> = new (...args: any[]) => T;

// @public
export class DataRowOutlet implements RowOutlet {
    constructor(viewContainer: ViewContainerRef, elementRef: ElementRef);
    // (undocumented)
    elementRef: ElementRef;
    // (undocumented)
    viewContainer: ViewContainerRef;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<DataRowOutlet, "[rowOutlet]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<DataRowOutlet, never>;
}

export { DataSource }

// @public
export class FooterRowOutlet implements RowOutlet {
    constructor(viewContainer: ViewContainerRef, elementRef: ElementRef);
    // (undocumented)
    elementRef: ElementRef;
    // (undocumented)
    viewContainer: ViewContainerRef;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<FooterRowOutlet, "[footerRowOutlet]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<FooterRowOutlet, never>;
}

// @public
export class HeaderRowOutlet implements RowOutlet {
    constructor(viewContainer: ViewContainerRef, elementRef: ElementRef);
    // (undocumented)
    elementRef: ElementRef;
    // (undocumented)
    viewContainer: ViewContainerRef;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<HeaderRowOutlet, "[headerRowOutlet]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<HeaderRowOutlet, never>;
}

// @public
export function mixinHasStickyInput<T extends Constructor<{}>>(base: T): CanStickCtor & T;

// @public
export class NoDataRowOutlet implements RowOutlet {
    constructor(viewContainer: ViewContainerRef, elementRef: ElementRef);
    // (undocumented)
    elementRef: ElementRef;
    // (undocumented)
    viewContainer: ViewContainerRef;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<NoDataRowOutlet, "[noDataRowOutlet]", never, {}, {}, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<NoDataRowOutlet, never>;
}

// @public
export interface RenderRow<T> {
    // (undocumented)
    data: T;
    // (undocumented)
    dataIndex: number;
    // (undocumented)
    rowDef: CdkRowDef<T>;
}

// @public
export interface RowContext<T> extends CdkCellOutletMultiRowContext<T>, CdkCellOutletRowContext<T> {
}

// @public
export interface RowOutlet {
    // (undocumented)
    viewContainer: ViewContainerRef;
}

// @public
export class _Schedule {
    // (undocumented)
    endTasks: (() => unknown)[];
    // (undocumented)
    tasks: (() => unknown)[];
}

// @public
export const STICKY_DIRECTIONS: StickyDirection[];

// @public
export const STICKY_POSITIONING_LISTENER: InjectionToken<StickyPositioningListener>;

// @public (undocumented)
export type StickyDirection = 'top' | 'bottom' | 'left' | 'right';

// @public (undocumented)
export type StickyOffset = number | null | undefined;

// @public
export interface StickyPositioningListener {
    stickyColumnsUpdated(update: StickyUpdate): void;
    stickyEndColumnsUpdated(update: StickyUpdate): void;
    stickyFooterRowsUpdated(update: StickyUpdate): void;
    stickyHeaderRowsUpdated(update: StickyUpdate): void;
}

// @public (undocumented)
export type StickySize = number | null | undefined;

// @public
export class StickyStyler {
    constructor(_isNativeHtmlTable: boolean, _stickCellCss: string, direction: Direction, _coalescedStyleScheduler: _CoalescedStyleScheduler, _isBrowser?: boolean, _needsPositionStickyOnElement?: boolean, _positionListener?: StickyPositioningListener | undefined);
    _addStickyStyle(element: HTMLElement, dir: StickyDirection, dirValue: number, isBorderElement: boolean): void;
    clearStickyPositioning(rows: HTMLElement[], stickyDirections: StickyDirection[]): void;
    // (undocumented)
    direction: Direction;
    _getCalculatedZIndex(element: HTMLElement): string;
    _getCellWidths(row: HTMLElement, recalculateCellWidths?: boolean): number[];
    _getStickyEndColumnPositions(widths: number[], stickyStates: boolean[]): number[];
    _getStickyStartColumnPositions(widths: number[], stickyStates: boolean[]): number[];
    _removeStickyStyle(element: HTMLElement, stickyDirections: StickyDirection[]): void;
    stickRows(rowsToStick: HTMLElement[], stickyStates: boolean[], position: 'top' | 'bottom'): void;
    updateStickyColumns(rows: HTMLElement[], stickyStartStates: boolean[], stickyEndStates: boolean[], recalculateCellWidths?: boolean): void;
    updateStickyFooterContainer(tableElement: Element, stickyStates: boolean[]): void;
}

// @public (undocumented)
export interface StickyUpdate {
    // (undocumented)
    elements?: readonly (HTMLElement[] | undefined)[];
    // (undocumented)
    offsets?: StickyOffset[];
    // (undocumented)
    sizes: StickySize[];
}

// @public
export const TEXT_COLUMN_OPTIONS: InjectionToken<TextColumnOptions<any>>;

// @public
export interface TextColumnOptions<T> {
    defaultDataAccessor?: (data: T, name: string) => string;
    defaultHeaderTextTransform?: (name: string) => string;
}

// (No @packageDocumentation comment for this package)

```