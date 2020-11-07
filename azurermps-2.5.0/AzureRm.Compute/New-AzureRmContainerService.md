---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 6d1a891dbef40a6556e3a8f2ca122f2c3b46cb28
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800182"
---
# <span data-ttu-id="021aa-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="021aa-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="021aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="021aa-102">SYNOPSIS</span></span>
<span data-ttu-id="021aa-103">建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="021aa-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="021aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="021aa-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="021aa-105">說明</span><span class="sxs-lookup"><span data-stu-id="021aa-105">DESCRIPTION</span></span>
<span data-ttu-id="021aa-106">**新的-AzureRmContainerService** Cmdlet 會建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="021aa-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="021aa-107">指定您可以使用 New-AzureRmContainerServiceConfig Cmdlet 建立的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="021aa-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="021aa-108">示例</span><span class="sxs-lookup"><span data-stu-id="021aa-108">EXAMPLES</span></span>

### <span data-ttu-id="021aa-109">範例1：建立容器服務</span><span class="sxs-lookup"><span data-stu-id="021aa-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="021aa-110">第一個命令會在指定的位置建立名為 ResourceGroup17 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="021aa-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="021aa-111">如需詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="021aa-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="021aa-112">第二個命令會建立一個容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="021aa-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="021aa-113">如需詳細資訊，請參閱 New-AzureRmContainerServiceConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="021aa-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="021aa-114">最後一個命令會針對儲存在 $Container 中的容器建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="021aa-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="021aa-115">該服務已命名為 csResourceGroup17。</span><span class="sxs-lookup"><span data-stu-id="021aa-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="021aa-116">參數</span><span class="sxs-lookup"><span data-stu-id="021aa-116">PARAMETERS</span></span>

### <span data-ttu-id="021aa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="021aa-117">-AsJob</span></span>
<span data-ttu-id="021aa-118">在背景中 RRun Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="021aa-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021aa-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="021aa-119">-ContainerService</span></span>
<span data-ttu-id="021aa-120">指定包含新服務屬性的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="021aa-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="021aa-121">若要取得 **ContainerService** 物件，請使用 New-AzureRmContainerServiceConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="021aa-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="021aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021aa-122">-DefaultProfile</span></span>
<span data-ttu-id="021aa-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="021aa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021aa-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="021aa-124">-Name</span></span>
<span data-ttu-id="021aa-125">指定此 Cmdlet 所建立之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="021aa-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="021aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="021aa-127">指定此 Cmdlet 用來部署容器服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="021aa-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="021aa-128">-確認</span><span class="sxs-lookup"><span data-stu-id="021aa-128">-Confirm</span></span>
<span data-ttu-id="021aa-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="021aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021aa-130">-WhatIf</span></span>
<span data-ttu-id="021aa-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="021aa-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="021aa-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="021aa-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021aa-133">CommonParameters</span></span>
<span data-ttu-id="021aa-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="021aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021aa-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="021aa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021aa-136">輸入</span><span class="sxs-lookup"><span data-stu-id="021aa-136">INPUTS</span></span>

### <span data-ttu-id="021aa-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="021aa-137">ContainerService</span></span>
<span data-ttu-id="021aa-138">形參 "ContainerService" 接受管線中 "ContainerService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="021aa-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="021aa-139">輸出</span><span class="sxs-lookup"><span data-stu-id="021aa-139">OUTPUTS</span></span>

### <span data-ttu-id="021aa-140">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="021aa-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="021aa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="021aa-141">NOTES</span></span>

## <span data-ttu-id="021aa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="021aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="021aa-143">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="021aa-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="021aa-144">新-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="021aa-144">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="021aa-145">移除-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="021aa-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="021aa-146">更新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="021aa-146">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


