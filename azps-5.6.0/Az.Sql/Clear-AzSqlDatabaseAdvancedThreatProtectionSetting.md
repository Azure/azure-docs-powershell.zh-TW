---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c9f8bfad95a7bbefd6e685701813d0c383f2b8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908729"
---
# <span data-ttu-id="52d07-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="52d07-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="52d07-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52d07-102">SYNOPSIS</span></span>
<span data-ttu-id="52d07-103">從資料庫移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="52d07-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="52d07-104">語法</span><span class="sxs-lookup"><span data-stu-id="52d07-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52d07-105">描述</span><span class="sxs-lookup"><span data-stu-id="52d07-105">DESCRIPTION</span></span>
<span data-ttu-id="52d07-106">**Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** Cmdlet 會從 AzureAzure SQL 資料庫移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="52d07-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="52d07-107">若要使用此 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數，以識別此 Cmdlet 會移除設定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="52d07-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="52d07-108">例子</span><span class="sxs-lookup"><span data-stu-id="52d07-108">EXAMPLES</span></span>

### <span data-ttu-id="52d07-109">範例 1：移除資料庫的進一步威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="52d07-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="52d07-110">此命令會從伺服器名為 Database01 的資料庫移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="52d07-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="52d07-111">參數</span><span class="sxs-lookup"><span data-stu-id="52d07-111">PARAMETERS</span></span>

### <span data-ttu-id="52d07-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52d07-112">-DatabaseName</span></span>
<span data-ttu-id="52d07-113">指定應該移除進位威脅防護設定的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="52d07-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="52d07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d07-114">-DefaultProfile</span></span>
<span data-ttu-id="52d07-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="52d07-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52d07-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52d07-116">-PassThru</span></span>
<span data-ttu-id="52d07-117">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="52d07-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52d07-118">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="52d07-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52d07-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d07-119">-ResourceGroupName</span></span>
<span data-ttu-id="52d07-120">指定伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="52d07-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="52d07-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52d07-121">-ServerName</span></span>
<span data-ttu-id="52d07-122">指定執行資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="52d07-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="52d07-123">-確認</span><span class="sxs-lookup"><span data-stu-id="52d07-123">-Confirm</span></span>
<span data-ttu-id="52d07-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="52d07-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52d07-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d07-125">-WhatIf</span></span>
<span data-ttu-id="52d07-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52d07-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52d07-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52d07-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52d07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d07-128">CommonParameters</span></span>
<span data-ttu-id="52d07-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52d07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d07-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52d07-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d07-131">輸入</span><span class="sxs-lookup"><span data-stu-id="52d07-131">INPUTS</span></span>

### <span data-ttu-id="52d07-132">System.String</span><span class="sxs-lookup"><span data-stu-id="52d07-132">System.String</span></span>

## <span data-ttu-id="52d07-133">輸出</span><span class="sxs-lookup"><span data-stu-id="52d07-133">OUTPUTS</span></span>

### <span data-ttu-id="52d07-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="52d07-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="52d07-135">筆記</span><span class="sxs-lookup"><span data-stu-id="52d07-135">NOTES</span></span>

## <span data-ttu-id="52d07-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="52d07-136">RELATED LINKS</span></span>

[<span data-ttu-id="52d07-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="52d07-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


