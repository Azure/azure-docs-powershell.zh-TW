---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 086085bd1a36c1508cf489d224ddd6bff4651c50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622652"
---
# <span data-ttu-id="91581-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="91581-101">Update-AzContainerService</span></span>

## <span data-ttu-id="91581-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91581-102">SYNOPSIS</span></span>
<span data-ttu-id="91581-103">更新容器服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="91581-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="91581-104">句法</span><span class="sxs-lookup"><span data-stu-id="91581-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91581-105">說明</span><span class="sxs-lookup"><span data-stu-id="91581-105">DESCRIPTION</span></span>
<span data-ttu-id="91581-106">**更新 AzContainerService** Cmdlet 會更新容器服務的狀態，以符合服務的本機實例。</span><span class="sxs-lookup"><span data-stu-id="91581-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="91581-107">示例</span><span class="sxs-lookup"><span data-stu-id="91581-107">EXAMPLES</span></span>

### <span data-ttu-id="91581-108">範例1：更新容器服務</span><span class="sxs-lookup"><span data-stu-id="91581-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="91581-109">這個命令會使用 Get-AzContainerService Cmdlet 來取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="91581-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="91581-110">命令會使用管線運算子，將該物件傳遞到 Remove-AzContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91581-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="91581-111">**移除-AzContainerServiceAgentPoolProfile** 會移除名為 AgentPool01 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="91581-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="91581-112">命令會將結果傳遞到 Add-AzContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91581-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="91581-113">[ **載入 AzContainerServiceAgentPoolProfile** ] 會新增具有名稱 AgentPool01 的設定檔，並具有指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="91581-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="91581-114">命令會將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91581-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="91581-115">目前的 Cmdlet 會更新容器服務，以反映此命令所做的變更。</span><span class="sxs-lookup"><span data-stu-id="91581-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="91581-116">參數</span><span class="sxs-lookup"><span data-stu-id="91581-116">PARAMETERS</span></span>

### <span data-ttu-id="91581-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91581-117">-AsJob</span></span>
<span data-ttu-id="91581-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="91581-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91581-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="91581-119">-ContainerService</span></span>
<span data-ttu-id="91581-120">指定包含變更的本機 **ContainerService** 物件。</span><span class="sxs-lookup"><span data-stu-id="91581-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91581-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91581-121">-DefaultProfile</span></span>
<span data-ttu-id="91581-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91581-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91581-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="91581-123">-Name</span></span>
<span data-ttu-id="91581-124">指定此 Cmdlet 更新之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="91581-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="91581-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91581-125">-ResourceGroupName</span></span>
<span data-ttu-id="91581-126">指定此 Cmdlet 更新之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="91581-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="91581-127">-確認</span><span class="sxs-lookup"><span data-stu-id="91581-127">-Confirm</span></span>
<span data-ttu-id="91581-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91581-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91581-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91581-129">-WhatIf</span></span>
<span data-ttu-id="91581-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91581-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91581-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91581-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91581-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91581-132">CommonParameters</span></span>
<span data-ttu-id="91581-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91581-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91581-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91581-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91581-135">輸入</span><span class="sxs-lookup"><span data-stu-id="91581-135">INPUTS</span></span>

### <span data-ttu-id="91581-136">System.object</span><span class="sxs-lookup"><span data-stu-id="91581-136">System.String</span></span>

### <span data-ttu-id="91581-137">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="91581-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="91581-138">輸出</span><span class="sxs-lookup"><span data-stu-id="91581-138">OUTPUTS</span></span>

### <span data-ttu-id="91581-139">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="91581-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="91581-140">筆記</span><span class="sxs-lookup"><span data-stu-id="91581-140">NOTES</span></span>

## <span data-ttu-id="91581-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="91581-141">RELATED LINKS</span></span>

[<span data-ttu-id="91581-142">附加 AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="91581-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="91581-143">AzContainerService</span><span class="sxs-lookup"><span data-stu-id="91581-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="91581-144">新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="91581-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="91581-145">移除-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="91581-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="91581-146">移除-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="91581-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)

