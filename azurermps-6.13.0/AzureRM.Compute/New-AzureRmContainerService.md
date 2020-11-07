---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: 9dd2018fe6f84ff4657da799fbcba720e8523bde
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93626662"
---
# <span data-ttu-id="d85f0-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d85f0-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="d85f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d85f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d85f0-103">建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="d85f0-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d85f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d85f0-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d85f0-105">說明</span><span class="sxs-lookup"><span data-stu-id="d85f0-105">DESCRIPTION</span></span>
<span data-ttu-id="d85f0-106">**新的-AzureRmContainerService** Cmdlet 會建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="d85f0-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="d85f0-107">指定您可以使用 New-AzureRmContainerServiceConfig Cmdlet 建立的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="d85f0-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="d85f0-108">示例</span><span class="sxs-lookup"><span data-stu-id="d85f0-108">EXAMPLES</span></span>

### <span data-ttu-id="d85f0-109">範例1：建立容器服務</span><span class="sxs-lookup"><span data-stu-id="d85f0-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="d85f0-110">第一個命令會在指定的位置建立名為 ResourceGroup17 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d85f0-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="d85f0-111">如需詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d85f0-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="d85f0-112">第二個命令會建立一個容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="d85f0-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="d85f0-113">如需詳細資訊，請參閱 New-AzureRmContainerServiceConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d85f0-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="d85f0-114">最後一個命令會針對儲存在 $Container 中的容器建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="d85f0-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="d85f0-115">該服務已命名為 csResourceGroup17。</span><span class="sxs-lookup"><span data-stu-id="d85f0-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="d85f0-116">參數</span><span class="sxs-lookup"><span data-stu-id="d85f0-116">PARAMETERS</span></span>

### <span data-ttu-id="d85f0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d85f0-117">-AsJob</span></span>
<span data-ttu-id="d85f0-118">在背景中 RRun Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="d85f0-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d85f0-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="d85f0-119">-ContainerService</span></span>
<span data-ttu-id="d85f0-120">指定包含新服務屬性的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="d85f0-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="d85f0-121">若要取得 **ContainerService** 物件，請使用 New-AzureRmContainerServiceConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d85f0-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="d85f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85f0-122">-DefaultProfile</span></span>
<span data-ttu-id="d85f0-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d85f0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d85f0-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d85f0-124">-Name</span></span>
<span data-ttu-id="d85f0-125">指定此 Cmdlet 所建立之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="d85f0-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d85f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d85f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="d85f0-127">指定此 Cmdlet 用來部署容器服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d85f0-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="d85f0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d85f0-128">-Confirm</span></span>
<span data-ttu-id="d85f0-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d85f0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d85f0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d85f0-130">-WhatIf</span></span>
<span data-ttu-id="d85f0-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d85f0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d85f0-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d85f0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d85f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85f0-133">CommonParameters</span></span>
<span data-ttu-id="d85f0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d85f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85f0-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d85f0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85f0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d85f0-136">INPUTS</span></span>

### <span data-ttu-id="d85f0-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d85f0-137">System.String</span></span>

### <span data-ttu-id="d85f0-138">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="d85f0-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="d85f0-139">參數： ContainerService (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d85f0-139">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="d85f0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d85f0-140">OUTPUTS</span></span>

### <span data-ttu-id="d85f0-141">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="d85f0-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d85f0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d85f0-142">NOTES</span></span>

## <span data-ttu-id="d85f0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d85f0-143">RELATED LINKS</span></span>

[<span data-ttu-id="d85f0-144">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d85f0-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="d85f0-145">新-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="d85f0-145">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="d85f0-146">移除-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d85f0-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="d85f0-147">更新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d85f0-147">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


