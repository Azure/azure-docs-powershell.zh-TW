---
Module Name: Az.FrontDoor
Module Guid: 91832aaa-dc11-4583-8239-adb7df531604
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
ms.openlocfilehash: 6f42c3e8588a40b2e912b2c93ec2bfb9534efeef
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611272"
---
# <span data-ttu-id="0701d-101">Az FrontDoor 模組</span><span class="sxs-lookup"><span data-stu-id="0701d-101">Az.FrontDoor Module</span></span>
## <span data-ttu-id="0701d-102">說明</span><span class="sxs-lookup"><span data-stu-id="0701d-102">Description</span></span>
<span data-ttu-id="0701d-103">本節中的主題檔在 Azure 資源管理器中，將 azure 前門服務的 Azure PowerShell Cmdlet 放在 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="0701d-103">The topics in this section document the Azure PowerShell cmdlets for Azure Front Door Service in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="0701d-104">FrontDoor 命名空間中存在 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0701d-104">The cmdlets exist in the Microsoft.Azure.Commands.FrontDoor namespace.</span></span>

## <span data-ttu-id="0701d-105">Az FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0701d-105">Az.FrontDoor Cmdlets</span></span>
### [<span data-ttu-id="0701d-106">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="0701d-106">Disable-AzFrontDoorCustomDomainHttps</span></span>](Disable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="0701d-107">停用自訂網域的 HTTPS</span><span class="sxs-lookup"><span data-stu-id="0701d-107">Disable HTTPS for a custom domain</span></span>

### [<span data-ttu-id="0701d-108">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="0701d-108">Enable-AzFrontDoorCustomDomainHttps</span></span>](Enable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="0701d-109">使用前門管理的憑證或從 Azure 金鑰保存庫使用自己的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="0701d-109">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

### [<span data-ttu-id="0701d-110">AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0701d-110">Get-AzFrontDoor</span></span>](Get-AzFrontDoor.md)
<span data-ttu-id="0701d-111">取得前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="0701d-111">Get Front Door load balancer</span></span>

### [<span data-ttu-id="0701d-112">AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="0701d-112">Get-AzFrontDoorFireWallPolicy</span></span>](Get-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="0701d-113">取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="0701d-113">Get WAF policy</span></span>

### [<span data-ttu-id="0701d-114">AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="0701d-114">Get-AzFrontDoorFrontendEndpoint</span></span>](Get-AzFrontDoorFrontendEndpoint.md)
<span data-ttu-id="0701d-115">取得前蓋前端端點。</span><span class="sxs-lookup"><span data-stu-id="0701d-115">Get a front door frontend endpoint.</span></span>

### [<span data-ttu-id="0701d-116">新-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0701d-116">New-AzFrontDoor</span></span>](New-AzFrontDoor.md)
<span data-ttu-id="0701d-117">建立新的 Azure 前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="0701d-117">Create a new Azure Front Door load balancer</span></span>

### [<span data-ttu-id="0701d-118">新-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="0701d-118">New-AzFrontDoorBackendObject</span></span>](New-AzFrontDoorBackendObject.md)
<span data-ttu-id="0701d-119">建立 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-119">Create a PSBackend object</span></span>

### [<span data-ttu-id="0701d-120">新-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="0701d-120">New-AzFrontDoorBackendPoolObject</span></span>](New-AzFrontDoorBackendPoolObject.md)
<span data-ttu-id="0701d-121">建立用來建立前門的 PSBackendPool 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-121">Create a PSBackendPool object for Front Door creation</span></span>

### [<span data-ttu-id="0701d-122">新-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="0701d-122">New-AzFrontDoorCustomRuleObject</span></span>](New-AzFrontDoorCustomRuleObject.md)
<span data-ttu-id="0701d-123">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-123">Create CustomRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="0701d-124">新-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="0701d-124">New-AzFrontDoorFireWallPolicy</span></span>](New-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="0701d-125">建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="0701d-125">Create WAF policy</span></span>

### [<span data-ttu-id="0701d-126">新-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0701d-126">New-AzFrontDoorFrontendEndpointObject</span></span>](New-AzFrontDoorFrontendEndpointObject.md)
<span data-ttu-id="0701d-127">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-127">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

### [<span data-ttu-id="0701d-128">新-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0701d-128">New-AzFrontDoorHealthProbeSettingObject</span></span>](New-AzFrontDoorHealthProbeSettingObject.md)
<span data-ttu-id="0701d-129">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-129">Create a PSHealthProbeSetting object for Front Door creation</span></span>

### [<span data-ttu-id="0701d-130">新-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="0701d-130">New-AzFrontDoorLoadBalancingSettingObject</span></span>](New-AzFrontDoorLoadBalancingSettingObject.md)
<span data-ttu-id="0701d-131">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-131">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

### [<span data-ttu-id="0701d-132">新-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0701d-132">New-AzFrontDoorManagedRuleObject</span></span>](New-AzFrontDoorManagedRuleObject.md)
<span data-ttu-id="0701d-133">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-133">Create ManagedRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="0701d-134">新-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="0701d-134">New-AzFrontDoorManagedRuleOverrideObject</span></span>](New-AzFrontDoorManagedRuleOverrideObject.md)
<span data-ttu-id="0701d-135">建立受管理的規則覆寫物件</span><span class="sxs-lookup"><span data-stu-id="0701d-135">Create managed rule override object</span></span>

### [<span data-ttu-id="0701d-136">新-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0701d-136">New-AzFrontDoorMatchConditionObject</span></span>](New-AzFrontDoorMatchConditionObject.md)
<span data-ttu-id="0701d-137">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-137">Create MatchCondition Object for WAF policy creation</span></span>

### [<span data-ttu-id="0701d-138">新-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="0701d-138">New-AzFrontDoorRoutingRuleObject</span></span>](New-AzFrontDoorRoutingRuleObject.md)
<span data-ttu-id="0701d-139">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="0701d-139">Create a PSRoutingRuleObject for Front Door creation</span></span>

### [<span data-ttu-id="0701d-140">新-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="0701d-140">New-AzFrontDoorRuleGroupOverrideObject</span></span>](New-AzFrontDoorRuleGroupOverrideObject.md)
<span data-ttu-id="0701d-141">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="0701d-141">Create RuleGroupOverride Object for WAF policy creation</span></span>

### [<span data-ttu-id="0701d-142">移除-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0701d-142">Remove-AzFrontDoor</span></span>](Remove-AzFrontDoor.md)
<span data-ttu-id="0701d-143">移除前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="0701d-143">Remove Front Door load balancer</span></span>

### [<span data-ttu-id="0701d-144">移除-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="0701d-144">Remove-AzFrontDoorContent</span></span>](Remove-AzFrontDoorContent.md)
<span data-ttu-id="0701d-145">移除前門中的內容</span><span class="sxs-lookup"><span data-stu-id="0701d-145">Remove contents in Front Door</span></span>

### [<span data-ttu-id="0701d-146">移除-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="0701d-146">Remove-AzFrontDoorFireWallPolicy</span></span>](Remove-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="0701d-147">移除 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="0701d-147">Remove WAF policy</span></span>

### [<span data-ttu-id="0701d-148">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0701d-148">Set-AzFrontDoor</span></span>](Set-AzFrontDoor.md)
<span data-ttu-id="0701d-149">更新前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="0701d-149">Update a Front Door load balancer</span></span>

### [<span data-ttu-id="0701d-150">更新-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="0701d-150">Update-AzFrontDoorFireWallPolicy</span></span>](Update-AzFrontDoorFireWallPolicy.md)
<span data-ttu-id="0701d-151">更新 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="0701d-151">Update WAF policy</span></span>

