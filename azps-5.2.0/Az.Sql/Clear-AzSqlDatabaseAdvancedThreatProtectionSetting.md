---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281650"
---
# <span data-ttu-id="76223-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="76223-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="76223-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76223-102">SYNOPSIS</span></span>
<span data-ttu-id="76223-103">從資料庫中移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="76223-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="76223-104">句法</span><span class="sxs-lookup"><span data-stu-id="76223-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76223-105">說明</span><span class="sxs-lookup"><span data-stu-id="76223-105">DESCRIPTION</span></span>
<span data-ttu-id="76223-106">**Clear AzSqlDatabaseAdvancedThreatProtectionSetting** Cmdlet 會從 AzureAzure SQL 資料庫中移除高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="76223-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="76223-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數來識別這個 Cmdlet 移除其設定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="76223-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="76223-108">示例</span><span class="sxs-lookup"><span data-stu-id="76223-108">EXAMPLES</span></span>

### <span data-ttu-id="76223-109">範例1：移除資料庫的高級威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="76223-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="76223-110">這個命令會從名為 Server01 的伺服器上名為 Database01 的資料庫中，移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="76223-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="76223-111">參數</span><span class="sxs-lookup"><span data-stu-id="76223-111">PARAMETERS</span></span>

### <span data-ttu-id="76223-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76223-112">-DatabaseName</span></span>
<span data-ttu-id="76223-113">指定應該移除高級威脅防護設定的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="76223-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76223-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76223-114">-DefaultProfile</span></span>
<span data-ttu-id="76223-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="76223-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76223-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76223-116">-PassThru</span></span>
<span data-ttu-id="76223-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="76223-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="76223-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="76223-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76223-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76223-119">-ResourceGroupName</span></span>
<span data-ttu-id="76223-120">指定伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76223-120">Specifies the name of the resource group the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76223-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="76223-121">-ServerName</span></span>
<span data-ttu-id="76223-122">指定資料庫在其上執行的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="76223-122">Specifies the name of a server on which the database runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76223-123">-確認</span><span class="sxs-lookup"><span data-stu-id="76223-123">-Confirm</span></span>
<span data-ttu-id="76223-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76223-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76223-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76223-125">-WhatIf</span></span>
<span data-ttu-id="76223-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76223-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76223-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76223-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76223-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76223-128">CommonParameters</span></span>
<span data-ttu-id="76223-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76223-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76223-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="76223-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76223-131">輸入</span><span class="sxs-lookup"><span data-stu-id="76223-131">INPUTS</span></span>

### <span data-ttu-id="76223-132">System.object</span><span class="sxs-lookup"><span data-stu-id="76223-132">System.String</span></span>

## <span data-ttu-id="76223-133">輸出</span><span class="sxs-lookup"><span data-stu-id="76223-133">OUTPUTS</span></span>

### <span data-ttu-id="76223-134">DatabaseThreatDetectionsettingsModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="76223-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="76223-135">筆記</span><span class="sxs-lookup"><span data-stu-id="76223-135">NOTES</span></span>

## <span data-ttu-id="76223-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="76223-136">RELATED LINKS</span></span>

[<span data-ttu-id="76223-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="76223-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


