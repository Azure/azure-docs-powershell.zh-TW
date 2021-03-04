---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4a576c930d8ff1c53c6c9e92c7d87664aef4da4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916876"
---
# <span data-ttu-id="3d004-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3d004-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3d004-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3d004-102">SYNOPSIS</span></span>
<span data-ttu-id="3d004-103">從伺服器移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="3d004-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="3d004-104">語法</span><span class="sxs-lookup"><span data-stu-id="3d004-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d004-105">描述</span><span class="sxs-lookup"><span data-stu-id="3d004-105">DESCRIPTION</span></span>
<span data-ttu-id="3d004-106">此Clear-AzSqlServerAdvancedThreatProtectionSetting Cmdlet 會從 Azure SQL 伺服器移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="3d004-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="3d004-107">若要使用此 Cmdlet，請指定 ResourceGroupName 和 ServerName 參數，以識別此 Cmdlet 會移除設定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d004-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="3d004-108">例子</span><span class="sxs-lookup"><span data-stu-id="3d004-108">EXAMPLES</span></span>

### <span data-ttu-id="3d004-109">範例 1：移除資料庫的進一步威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="3d004-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="3d004-110">此命令會從伺服器名稱為 Server01 移除進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="3d004-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="3d004-111">參數</span><span class="sxs-lookup"><span data-stu-id="3d004-111">PARAMETERS</span></span>

### <span data-ttu-id="3d004-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d004-112">-DefaultProfile</span></span>
<span data-ttu-id="3d004-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3d004-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d004-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d004-114">-PassThru</span></span>
<span data-ttu-id="3d004-115">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3d004-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3d004-116">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3d004-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3d004-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d004-117">-ResourceGroupName</span></span>
<span data-ttu-id="3d004-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3d004-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="3d004-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d004-119">-ServerName</span></span>
<span data-ttu-id="3d004-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d004-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d004-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3d004-121">-Confirm</span></span>
<span data-ttu-id="3d004-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3d004-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d004-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d004-123">-WhatIf</span></span>
<span data-ttu-id="3d004-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d004-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d004-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d004-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d004-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d004-126">CommonParameters</span></span>
<span data-ttu-id="3d004-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3d004-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d004-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d004-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d004-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3d004-129">INPUTS</span></span>

### <span data-ttu-id="3d004-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3d004-130">System.String</span></span>

## <span data-ttu-id="3d004-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3d004-131">OUTPUTS</span></span>

### <span data-ttu-id="3d004-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="3d004-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="3d004-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3d004-133">NOTES</span></span>

## <span data-ttu-id="3d004-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d004-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d004-135">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3d004-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

