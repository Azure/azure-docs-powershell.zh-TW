---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143378"
---
# <span data-ttu-id="356e3-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="356e3-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="356e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="356e3-102">SYNOPSIS</span></span>
<span data-ttu-id="356e3-103">從容器服務移除代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="356e3-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="356e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="356e3-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="356e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="356e3-105">DESCRIPTION</span></span>
<span data-ttu-id="356e3-106">**AzContainerServiceAgentPoolProfile** Cmdlet 會從容器服務中移除代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="356e3-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="356e3-107">示例</span><span class="sxs-lookup"><span data-stu-id="356e3-107">EXAMPLES</span></span>

### <span data-ttu-id="356e3-108">範例1：從容器服務移除設定檔</span><span class="sxs-lookup"><span data-stu-id="356e3-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="356e3-109">第一個命令會使用 Get-AzContainerService Cmdlet 來取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="356e3-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="356e3-110">該命令會將服務儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="356e3-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="356e3-111">第二個命令會從 $Container 的容器服務中移除名為 AgentPool01 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="356e3-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="356e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="356e3-112">PARAMETERS</span></span>

### <span data-ttu-id="356e3-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="356e3-113">-ContainerService</span></span>
<span data-ttu-id="356e3-114">指定此 Cmdlet 從中移除代理程式組件設定檔的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="356e3-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="356e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356e3-115">-DefaultProfile</span></span>
<span data-ttu-id="356e3-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="356e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="356e3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="356e3-117">-Name</span></span>
<span data-ttu-id="356e3-118">指定此 Cmdlet 移除的代理池設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="356e3-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="356e3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="356e3-119">-Confirm</span></span>
<span data-ttu-id="356e3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="356e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356e3-121">-WhatIf</span></span>
<span data-ttu-id="356e3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="356e3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="356e3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="356e3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356e3-124">CommonParameters</span></span>
<span data-ttu-id="356e3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="356e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356e3-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="356e3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356e3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="356e3-127">INPUTS</span></span>

### <span data-ttu-id="356e3-128">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="356e3-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="356e3-129">System.object</span><span class="sxs-lookup"><span data-stu-id="356e3-129">System.String</span></span>

## <span data-ttu-id="356e3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="356e3-130">OUTPUTS</span></span>

### <span data-ttu-id="356e3-131">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="356e3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="356e3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="356e3-132">NOTES</span></span>

## <span data-ttu-id="356e3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="356e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="356e3-134">附加 AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="356e3-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="356e3-135">AzContainerService</span><span class="sxs-lookup"><span data-stu-id="356e3-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


