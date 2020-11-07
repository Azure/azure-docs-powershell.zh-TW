---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 215ab742a91bc70c51860950acedb3449966bda2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790854"
---
# <span data-ttu-id="b79fb-101">Clear-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="b79fb-101">Clear-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="b79fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b79fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b79fb-103">從伺服器移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="b79fb-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="b79fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="b79fb-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b79fb-105">說明</span><span class="sxs-lookup"><span data-stu-id="b79fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b79fb-106">Clear-AzSqlServerAdvancedThreatProtectionSettings Cmdlet 會從 Azure SQL server 中移除高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="b79fb-106">The Clear-AzSqlServerAdvancedThreatProtectionSettings cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="b79fb-107">若要使用這個 Cmdlet，請指定 ResourceGroupName 和 ServerName 參數來識別這個 Cmdlet 移除其設定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b79fb-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="b79fb-108">示例</span><span class="sxs-lookup"><span data-stu-id="b79fb-108">EXAMPLES</span></span>

### <span data-ttu-id="b79fb-109">範例1：移除資料庫的高級威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="b79fb-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="b79fb-110">這個命令會從名為 Server01 的伺服器中移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="b79fb-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="b79fb-111">參數</span><span class="sxs-lookup"><span data-stu-id="b79fb-111">PARAMETERS</span></span>

### <span data-ttu-id="b79fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79fb-112">-DefaultProfile</span></span>
<span data-ttu-id="b79fb-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b79fb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b79fb-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b79fb-114">-PassThru</span></span>
<span data-ttu-id="b79fb-115">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b79fb-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b79fb-116">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b79fb-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b79fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b79fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="b79fb-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b79fb-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="b79fb-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b79fb-119">-ServerName</span></span>
<span data-ttu-id="b79fb-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b79fb-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="b79fb-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b79fb-121">-Confirm</span></span>
<span data-ttu-id="b79fb-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b79fb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b79fb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b79fb-123">-WhatIf</span></span>
<span data-ttu-id="b79fb-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b79fb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b79fb-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b79fb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b79fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79fb-126">CommonParameters</span></span>
<span data-ttu-id="b79fb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b79fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79fb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b79fb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79fb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b79fb-129">INPUTS</span></span>

### <span data-ttu-id="b79fb-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b79fb-130">System.String</span></span>

## <span data-ttu-id="b79fb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b79fb-131">OUTPUTS</span></span>

### <span data-ttu-id="b79fb-132">ServerThreatDetectionsettingsModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="b79fb-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="b79fb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b79fb-133">NOTES</span></span>

## <span data-ttu-id="b79fb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b79fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="b79fb-135">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b79fb-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

