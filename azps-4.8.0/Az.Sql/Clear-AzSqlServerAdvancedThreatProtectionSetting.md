---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970149"
---
# <span data-ttu-id="cbcac-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cbcac-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cbcac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbcac-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcac-103">從伺服器移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="cbcac-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="cbcac-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbcac-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbcac-105">說明</span><span class="sxs-lookup"><span data-stu-id="cbcac-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcac-106">Clear-AzSqlServerAdvancedThreatProtectionSetting Cmdlet 會從 Azure SQL server 中移除高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="cbcac-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="cbcac-107">若要使用這個 Cmdlet，請指定 ResourceGroupName 和 ServerName 參數來識別這個 Cmdlet 移除其設定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="cbcac-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="cbcac-108">示例</span><span class="sxs-lookup"><span data-stu-id="cbcac-108">EXAMPLES</span></span>

### <span data-ttu-id="cbcac-109">範例1：移除資料庫的高級威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="cbcac-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="cbcac-110">這個命令會從名為 Server01 的伺服器中移除 [高級威脅防護] 設定。</span><span class="sxs-lookup"><span data-stu-id="cbcac-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="cbcac-111">參數</span><span class="sxs-lookup"><span data-stu-id="cbcac-111">PARAMETERS</span></span>

### <span data-ttu-id="cbcac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcac-112">-DefaultProfile</span></span>
<span data-ttu-id="cbcac-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cbcac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbcac-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbcac-114">-PassThru</span></span>
<span data-ttu-id="cbcac-115">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cbcac-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cbcac-116">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cbcac-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cbcac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcac-117">-ResourceGroupName</span></span>
<span data-ttu-id="cbcac-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbcac-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="cbcac-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbcac-119">-ServerName</span></span>
<span data-ttu-id="cbcac-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbcac-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="cbcac-121">-確認</span><span class="sxs-lookup"><span data-stu-id="cbcac-121">-Confirm</span></span>
<span data-ttu-id="cbcac-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbcac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbcac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbcac-123">-WhatIf</span></span>
<span data-ttu-id="cbcac-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbcac-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbcac-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbcac-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbcac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcac-126">CommonParameters</span></span>
<span data-ttu-id="cbcac-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbcac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcac-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cbcac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcac-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cbcac-129">INPUTS</span></span>

### <span data-ttu-id="cbcac-130">System.object</span><span class="sxs-lookup"><span data-stu-id="cbcac-130">System.String</span></span>

## <span data-ttu-id="cbcac-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cbcac-131">OUTPUTS</span></span>

### <span data-ttu-id="cbcac-132">ServerThreatDetectionsettingsModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="cbcac-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="cbcac-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cbcac-133">NOTES</span></span>

## <span data-ttu-id="cbcac-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbcac-134">RELATED LINKS</span></span>

[<span data-ttu-id="cbcac-135">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cbcac-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

