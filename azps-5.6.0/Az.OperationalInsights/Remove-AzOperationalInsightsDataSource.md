---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 1a99f06fac37c0d96a159b0c17afc606d850ee65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911585"
---
# <span data-ttu-id="04280-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="04280-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="04280-102">簡介</span><span class="sxs-lookup"><span data-stu-id="04280-102">SYNOPSIS</span></span>
<span data-ttu-id="04280-103">刪除資料來源。</span><span class="sxs-lookup"><span data-stu-id="04280-103">Deletes a data source.</span></span>

## <span data-ttu-id="04280-104">語法</span><span class="sxs-lookup"><span data-stu-id="04280-104">SYNTAX</span></span>

### <span data-ttu-id="04280-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="04280-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04280-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="04280-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04280-107">描述</span><span class="sxs-lookup"><span data-stu-id="04280-107">DESCRIPTION</span></span>
<span data-ttu-id="04280-108">**Remove-AzOperationalInsightsDataSource** Cmdlet 會刪除資料來源。</span><span class="sxs-lookup"><span data-stu-id="04280-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="04280-109">例子</span><span class="sxs-lookup"><span data-stu-id="04280-109">EXAMPLES</span></span>

## <span data-ttu-id="04280-110">參數</span><span class="sxs-lookup"><span data-stu-id="04280-110">PARAMETERS</span></span>

### <span data-ttu-id="04280-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04280-111">-DefaultProfile</span></span>
<span data-ttu-id="04280-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="04280-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04280-113">-強制</span><span class="sxs-lookup"><span data-stu-id="04280-113">-Force</span></span>
<span data-ttu-id="04280-114">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="04280-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="04280-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="04280-115">-Name</span></span>
<span data-ttu-id="04280-116">指定要刪除的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="04280-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04280-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04280-117">-ResourceGroupName</span></span>
<span data-ttu-id="04280-118">指定包含電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="04280-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04280-119">-工作區</span><span class="sxs-lookup"><span data-stu-id="04280-119">-Workspace</span></span>
<span data-ttu-id="04280-120">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="04280-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04280-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="04280-121">-WorkspaceName</span></span>
<span data-ttu-id="04280-122">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="04280-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04280-123">-確認</span><span class="sxs-lookup"><span data-stu-id="04280-123">-Confirm</span></span>
<span data-ttu-id="04280-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="04280-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04280-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04280-125">-WhatIf</span></span>
<span data-ttu-id="04280-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04280-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04280-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04280-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04280-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04280-128">CommonParameters</span></span>
<span data-ttu-id="04280-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="04280-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04280-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="04280-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04280-131">輸入</span><span class="sxs-lookup"><span data-stu-id="04280-131">INPUTS</span></span>

### <span data-ttu-id="04280-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="04280-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="04280-133">System.String</span><span class="sxs-lookup"><span data-stu-id="04280-133">System.String</span></span>

## <span data-ttu-id="04280-134">輸出</span><span class="sxs-lookup"><span data-stu-id="04280-134">OUTPUTS</span></span>

### <span data-ttu-id="04280-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="04280-135">System.Void</span></span>

## <span data-ttu-id="04280-136">筆記</span><span class="sxs-lookup"><span data-stu-id="04280-136">NOTES</span></span>
* <span data-ttu-id="04280-137">關鍵字：azure、azurerm、arm、資源、管理、主管、營運、深入資訊</span><span class="sxs-lookup"><span data-stu-id="04280-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="04280-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="04280-138">RELATED LINKS</span></span>

[<span data-ttu-id="04280-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="04280-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="04280-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="04280-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


