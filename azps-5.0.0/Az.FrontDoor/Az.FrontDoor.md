---
Module Name: Az.FrontDoor
Module Guid: 91832aaa-dc11-4583-8239-adb7df531604
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
ms.openlocfilehash: 5039a5684dfc24a05f2d79e49397b8d064bc6a3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138878"
---
# <span data-ttu-id="10865-101">Az FrontDoor 模組</span><span class="sxs-lookup"><span data-stu-id="10865-101">Az.FrontDoor Module</span></span>
## <span data-ttu-id="10865-102">說明</span><span class="sxs-lookup"><span data-stu-id="10865-102">Description</span></span>
<span data-ttu-id="10865-103">本節中的主題檔在 Azure 資源管理器中，將 azure 前門服務的 Azure PowerShell Cmdlet 放在 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="10865-103">The topics in this section document the Azure PowerShell cmdlets for Azure Front Door Service in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="10865-104">FrontDoor 命名空間中存在 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10865-104">The cmdlets exist in the Microsoft.Azure.Commands.FrontDoor namespace.</span></span>

## <span data-ttu-id="10865-105">Az FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="10865-105">Az.FrontDoor Cmdlets</span></span>
### [<span data-ttu-id="10865-106">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="10865-106">Disable-AzFrontDoorCustomDomainHttps</span></span>](Disable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="10865-107">停用自訂網域的 HTTPS</span><span class="sxs-lookup"><span data-stu-id="10865-107">Disable HTTPS for a custom domain</span></span>

### [<span data-ttu-id="10865-108">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="10865-108">Enable-AzFrontDoorCustomDomainHttps</span></span>](Enable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="10865-109">使用前門管理的憑證或從 Azure 金鑰保存庫使用自己的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="10865-109">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

### [<span data-ttu-id="10865-110">AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="10865-110">Get-AzFrontDoor</span></span>](Get-AzFrontDoor.md)
<span data-ttu-id="10865-111">取得前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="10865-111">Get Front Door load balancer</span></span>

### [<span data-ttu-id="10865-112">AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="10865-112">Get-AzFrontDoorFrontendEndpoint</span></span>](Get-AzFrontDoorFrontendEndpoint.md)
<span data-ttu-id="10865-113">取得前蓋前端端點。</span><span class="sxs-lookup"><span data-stu-id="10865-113">Get a front door frontend endpoint.</span></span>

### [<span data-ttu-id="10865-114">AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="10865-114">Get-AzFrontDoorRulesEngine</span></span>](Get-AzFrontDoorRulesEngine.md)
<span data-ttu-id="10865-115">取得規則引擎設定。</span><span class="sxs-lookup"><span data-stu-id="10865-115">Get Rules Engine configurations.</span></span>

### [<span data-ttu-id="10865-116">AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="10865-116">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>](Get-AzFrontDoorWafManagedRuleSetDefinition.md)
<span data-ttu-id="10865-117">取得 WAF managed 規則集定義</span><span class="sxs-lookup"><span data-stu-id="10865-117">Get WAF managed rule set definitions</span></span>

### [<span data-ttu-id="10865-118">AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="10865-118">Get-AzFrontDoorWafPolicy</span></span>](Get-AzFrontDoorWafPolicy.md)
<span data-ttu-id="10865-119">取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="10865-119">Get WAF policy</span></span>

### [<span data-ttu-id="10865-120">新-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="10865-120">New-AzFrontDoor</span></span>](New-AzFrontDoor.md)
<span data-ttu-id="10865-121">建立新的 Azure 前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="10865-121">Create a new Azure Front Door load balancer</span></span>

### [<span data-ttu-id="10865-122">新-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="10865-122">New-AzFrontDoorBackendObject</span></span>](New-AzFrontDoorBackendObject.md)
<span data-ttu-id="10865-123">建立 PSBackend 物件</span><span class="sxs-lookup"><span data-stu-id="10865-123">Create a PSBackend object</span></span>

### [<span data-ttu-id="10865-124">新-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="10865-124">New-AzFrontDoorBackendPoolObject</span></span>](New-AzFrontDoorBackendPoolObject.md)
<span data-ttu-id="10865-125">建立用來建立前門的 PSBackendPool 物件</span><span class="sxs-lookup"><span data-stu-id="10865-125">Create a PSBackendPool object for Front Door creation</span></span>

### [<span data-ttu-id="10865-126">新-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="10865-126">New-AzFrontDoorBackendPoolsSettingObject</span></span>](New-AzFrontDoorBackendPoolsSettingObject.md)
<span data-ttu-id="10865-127">建立用來建立前門的 PSBackendPoolsSetting 物件。</span><span class="sxs-lookup"><span data-stu-id="10865-127">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

### [<span data-ttu-id="10865-128">新-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="10865-128">New-AzFrontDoorFrontendEndpointObject</span></span>](New-AzFrontDoorFrontendEndpointObject.md)
<span data-ttu-id="10865-129">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="10865-129">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

### [<span data-ttu-id="10865-130">新-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="10865-130">New-AzFrontDoorHeaderActionObject</span></span>](New-AzFrontDoorHeaderActionObject.md)
<span data-ttu-id="10865-131">建立 PSHeaderAction 物件。</span><span class="sxs-lookup"><span data-stu-id="10865-131">Create PSHeaderAction object.</span></span>

### [<span data-ttu-id="10865-132">新-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="10865-132">New-AzFrontDoorHealthProbeSettingObject</span></span>](New-AzFrontDoorHealthProbeSettingObject.md)
<span data-ttu-id="10865-133">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="10865-133">Create a PSHealthProbeSetting object for Front Door creation</span></span>

### [<span data-ttu-id="10865-134">新-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="10865-134">New-AzFrontDoorLoadBalancingSettingObject</span></span>](New-AzFrontDoorLoadBalancingSettingObject.md)
<span data-ttu-id="10865-135">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="10865-135">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

### [<span data-ttu-id="10865-136">新-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="10865-136">New-AzFrontDoorRoutingRuleObject</span></span>](New-AzFrontDoorRoutingRuleObject.md)
<span data-ttu-id="10865-137">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="10865-137">Create a PSRoutingRuleObject for Front Door creation</span></span>

### [<span data-ttu-id="10865-138">新-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="10865-138">New-AzFrontDoorRulesEngine</span></span>](New-AzFrontDoorRulesEngine.md)
<span data-ttu-id="10865-139">針對指定的前門建立新的規則引擎配置。</span><span class="sxs-lookup"><span data-stu-id="10865-139">Create a new rules engine configuration for a specified front door.</span></span> 

### [<span data-ttu-id="10865-140">新-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="10865-140">New-AzFrontDoorRulesEngineActionObject</span></span>](New-AzFrontDoorRulesEngineActionObject.md)
<span data-ttu-id="10865-141">建立建立規則引擎規則的 PSRulesEngineAction 物件。</span><span class="sxs-lookup"><span data-stu-id="10865-141">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

### [<span data-ttu-id="10865-142">新-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="10865-142">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>](New-AzFrontDoorRulesEngineMatchConditionObject.md)
<span data-ttu-id="10865-143">建立建立規則引擎規則的 PSRulesEngineMatchCondition 物件。</span><span class="sxs-lookup"><span data-stu-id="10865-143">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

### [<span data-ttu-id="10865-144">新-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="10865-144">New-AzFrontDoorRulesEngineRuleObject</span></span>](New-AzFrontDoorRulesEngineRuleObject.md)
<span data-ttu-id="10865-145">建立規則引擎建立的 PSRulesEngineRule 物件。</span><span class="sxs-lookup"><span data-stu-id="10865-145">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

### [<span data-ttu-id="10865-146">新-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="10865-146">New-AzFrontDoorWafCustomRuleObject</span></span>](New-AzFrontDoorWafCustomRuleObject.md)
<span data-ttu-id="10865-147">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="10865-147">Create CustomRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="10865-148">新-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="10865-148">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>](New-AzFrontDoorWafManagedRuleExclusionObject.md)
<span data-ttu-id="10865-149">針對 WAF 受管理的規則集、群組或規則，建立受管理規則的排除物件。</span><span class="sxs-lookup"><span data-stu-id="10865-149">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

### [<span data-ttu-id="10865-150">新-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="10865-150">New-AzFrontDoorWafManagedRuleObject</span></span>](New-AzFrontDoorWafManagedRuleObject.md)
<span data-ttu-id="10865-151">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="10865-151">Create ManagedRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="10865-152">新-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="10865-152">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>](New-AzFrontDoorWafManagedRuleOverrideObject.md)
<span data-ttu-id="10865-153">建立受管理的規則覆寫物件</span><span class="sxs-lookup"><span data-stu-id="10865-153">Create managed rule override object</span></span>

### [<span data-ttu-id="10865-154">新-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="10865-154">New-AzFrontDoorWafMatchConditionObject</span></span>](New-AzFrontDoorWafMatchConditionObject.md)
<span data-ttu-id="10865-155">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="10865-155">Create MatchCondition Object for WAF policy creation</span></span>

### [<span data-ttu-id="10865-156">新-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="10865-156">New-AzFrontDoorWafPolicy</span></span>](New-AzFrontDoorWafPolicy.md)
<span data-ttu-id="10865-157">建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="10865-157">Create WAF policy</span></span>

### [<span data-ttu-id="10865-158">新-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="10865-158">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](New-AzFrontDoorWafRuleGroupOverrideObject.md)
<span data-ttu-id="10865-159">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="10865-159">Create RuleGroupOverride Object for WAF policy creation</span></span>

### [<span data-ttu-id="10865-160">移除-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="10865-160">Remove-AzFrontDoor</span></span>](Remove-AzFrontDoor.md)
<span data-ttu-id="10865-161">移除前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="10865-161">Remove Front Door load balancer</span></span>

### [<span data-ttu-id="10865-162">移除-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="10865-162">Remove-AzFrontDoorContent</span></span>](Remove-AzFrontDoorContent.md)
<span data-ttu-id="10865-163">移除前門中的內容</span><span class="sxs-lookup"><span data-stu-id="10865-163">Remove contents in Front Door</span></span>

### [<span data-ttu-id="10865-164">移除-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="10865-164">Remove-AzFrontDoorRulesEngine</span></span>](Remove-AzFrontDoorRulesEngine.md)
<span data-ttu-id="10865-165">從前門移除規則引擎</span><span class="sxs-lookup"><span data-stu-id="10865-165">Remove Rules Engine from Front Door</span></span>

### [<span data-ttu-id="10865-166">移除-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="10865-166">Remove-AzFrontDoorWafPolicy</span></span>](Remove-AzFrontDoorWafPolicy.md)
<span data-ttu-id="10865-167">移除 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="10865-167">Remove WAF policy</span></span>

### [<span data-ttu-id="10865-168">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="10865-168">Set-AzFrontDoor</span></span>](Set-AzFrontDoor.md)
<span data-ttu-id="10865-169">更新前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="10865-169">Update a Front Door load balancer</span></span>

### [<span data-ttu-id="10865-170">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="10865-170">Set-AzFrontDoorRulesEngine</span></span>](Set-AzFrontDoorRulesEngine.md)
<span data-ttu-id="10865-171">更新規則引擎。</span><span class="sxs-lookup"><span data-stu-id="10865-171">Update a Rules Engine.</span></span>

### [<span data-ttu-id="10865-172">更新-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="10865-172">Update-AzFrontDoorWafPolicy</span></span>](Update-AzFrontDoorWafPolicy.md)
<span data-ttu-id="10865-173">更新 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="10865-173">Update WAF policy</span></span>

