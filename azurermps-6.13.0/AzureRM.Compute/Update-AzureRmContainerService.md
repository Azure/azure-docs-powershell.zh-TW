---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: bacc9366292225e07fd07ac65726018f1d1879e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445644"
---
# <span data-ttu-id="1050c-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1050c-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="1050c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1050c-102">SYNOPSIS</span></span>
<span data-ttu-id="1050c-103">更新容器服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="1050c-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1050c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1050c-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1050c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1050c-105">DESCRIPTION</span></span>
<span data-ttu-id="1050c-106">**更新 AzureRmContainerService** Cmdlet 會更新容器服務的狀態，以符合服務的本機實例。</span><span class="sxs-lookup"><span data-stu-id="1050c-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="1050c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1050c-107">EXAMPLES</span></span>

### <span data-ttu-id="1050c-108">範例1：更新容器服務</span><span class="sxs-lookup"><span data-stu-id="1050c-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="1050c-109">這個命令會使用 Get-AzureRmContainerService Cmdlet 來取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="1050c-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="1050c-110">命令會使用管線運算子，將該物件傳遞到 Remove-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1050c-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1050c-111">**移除-AzureRmContainerServiceAgentPoolProfile** 會移除名為 AgentPool01 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="1050c-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="1050c-112">命令會將結果傳遞到 Add-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1050c-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="1050c-113">[ **載入 AzureRmContainerServiceAgentPoolProfile** ] 會新增具有名稱 AgentPool01 的設定檔，並具有指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="1050c-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="1050c-114">命令會將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1050c-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="1050c-115">目前的 Cmdlet 會更新容器服務，以反映此命令所做的變更。</span><span class="sxs-lookup"><span data-stu-id="1050c-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="1050c-116">參數</span><span class="sxs-lookup"><span data-stu-id="1050c-116">PARAMETERS</span></span>

### <span data-ttu-id="1050c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1050c-117">-AsJob</span></span>
<span data-ttu-id="1050c-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1050c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1050c-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="1050c-119">-ContainerService</span></span>
<span data-ttu-id="1050c-120">指定包含變更的本機 **ContainerService** 物件。</span><span class="sxs-lookup"><span data-stu-id="1050c-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1050c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1050c-121">-DefaultProfile</span></span>
<span data-ttu-id="1050c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1050c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1050c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1050c-123">-Name</span></span>
<span data-ttu-id="1050c-124">指定此 Cmdlet 更新之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="1050c-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1050c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1050c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1050c-126">指定此 Cmdlet 更新之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="1050c-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1050c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1050c-127">-Confirm</span></span>
<span data-ttu-id="1050c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1050c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1050c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1050c-129">-WhatIf</span></span>
<span data-ttu-id="1050c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1050c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1050c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1050c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1050c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1050c-132">CommonParameters</span></span>
<span data-ttu-id="1050c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1050c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1050c-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1050c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1050c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1050c-135">INPUTS</span></span>

### <span data-ttu-id="1050c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="1050c-136">System.String</span></span>

### <span data-ttu-id="1050c-137">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1050c-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="1050c-138">參數： ContainerService (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1050c-138">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="1050c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1050c-139">OUTPUTS</span></span>

### <span data-ttu-id="1050c-140">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1050c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="1050c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1050c-141">NOTES</span></span>

## <span data-ttu-id="1050c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1050c-142">RELATED LINKS</span></span>

[<span data-ttu-id="1050c-143">附加 AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1050c-143">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="1050c-144">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1050c-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="1050c-145">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1050c-145">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="1050c-146">移除-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1050c-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="1050c-147">移除-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1050c-147">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


