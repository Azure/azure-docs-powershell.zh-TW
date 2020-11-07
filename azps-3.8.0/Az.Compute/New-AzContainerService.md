---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957420"
---
# <span data-ttu-id="5f85e-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5f85e-101">New-AzContainerService</span></span>

## <span data-ttu-id="5f85e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f85e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f85e-103">建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="5f85e-103">Creates a container service.</span></span>

## <span data-ttu-id="5f85e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f85e-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f85e-105">說明</span><span class="sxs-lookup"><span data-stu-id="5f85e-105">DESCRIPTION</span></span>
<span data-ttu-id="5f85e-106">**新的-AzContainerService** Cmdlet 會建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="5f85e-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="5f85e-107">指定您可以使用 New-AzContainerServiceConfig Cmdlet 建立的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="5f85e-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="5f85e-108">示例</span><span class="sxs-lookup"><span data-stu-id="5f85e-108">EXAMPLES</span></span>

### <span data-ttu-id="5f85e-109">範例1：建立容器服務</span><span class="sxs-lookup"><span data-stu-id="5f85e-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="5f85e-110">第一個命令會在指定的位置建立名為 ResourceGroup17 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5f85e-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="5f85e-111">如需詳細資訊，請參閱 New-AzResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f85e-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="5f85e-112">第二個命令會建立一個容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="5f85e-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5f85e-113">如需詳細資訊，請參閱 New-AzContainerServiceConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f85e-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="5f85e-114">最後一個命令會針對儲存在 $Container 中的容器建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="5f85e-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="5f85e-115">該服務已命名為 csResourceGroup17。</span><span class="sxs-lookup"><span data-stu-id="5f85e-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="5f85e-116">參數</span><span class="sxs-lookup"><span data-stu-id="5f85e-116">PARAMETERS</span></span>

### <span data-ttu-id="5f85e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f85e-117">-AsJob</span></span>
<span data-ttu-id="5f85e-118">在背景中 RRun Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="5f85e-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5f85e-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="5f85e-119">-ContainerService</span></span>
<span data-ttu-id="5f85e-120">指定包含新服務屬性的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="5f85e-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="5f85e-121">若要取得 **ContainerService** 物件，請使用 New-AzContainerServiceConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f85e-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="5f85e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f85e-122">-DefaultProfile</span></span>
<span data-ttu-id="5f85e-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f85e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f85e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f85e-124">-Name</span></span>
<span data-ttu-id="5f85e-125">指定此 Cmdlet 所建立之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f85e-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5f85e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f85e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5f85e-127">指定此 Cmdlet 用來部署容器服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5f85e-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="5f85e-128">-確認</span><span class="sxs-lookup"><span data-stu-id="5f85e-128">-Confirm</span></span>
<span data-ttu-id="5f85e-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f85e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f85e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f85e-130">-WhatIf</span></span>
<span data-ttu-id="5f85e-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f85e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f85e-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f85e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f85e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f85e-133">CommonParameters</span></span>
<span data-ttu-id="5f85e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f85e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f85e-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5f85e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f85e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5f85e-136">INPUTS</span></span>

### <span data-ttu-id="5f85e-137">System.object</span><span class="sxs-lookup"><span data-stu-id="5f85e-137">System.String</span></span>

### <span data-ttu-id="5f85e-138">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="5f85e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="5f85e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5f85e-139">OUTPUTS</span></span>

### <span data-ttu-id="5f85e-140">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="5f85e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="5f85e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5f85e-141">NOTES</span></span>

## <span data-ttu-id="5f85e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f85e-142">RELATED LINKS</span></span>

[<span data-ttu-id="5f85e-143">AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5f85e-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="5f85e-144">新-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="5f85e-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="5f85e-145">移除-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5f85e-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="5f85e-146">更新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5f85e-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


