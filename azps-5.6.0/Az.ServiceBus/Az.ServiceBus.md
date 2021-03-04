---
Module Name: Az.ServiceBus
Module Guid: cc69c625-e961-43f4-8b50-0061eba6e4b6
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicebus
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
ms.openlocfilehash: 7f5c2658b32b0bf713dc131474eca30e57955187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916357"
---
# <span data-ttu-id="60a36-101">Az.ServiceBus 模組</span><span class="sxs-lookup"><span data-stu-id="60a36-101">Az.ServiceBus Module</span></span>
## <span data-ttu-id="60a36-102">描述</span><span class="sxs-lookup"><span data-stu-id="60a36-102">Description</span></span>
<span data-ttu-id="60a36-103">本主題顯示 Azure Service Bus Cmdlet 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="60a36-103">This topic displays help topics for the Azure Service Bus cmdlets.</span></span>

## <span data-ttu-id="60a36-104">Az.ServiceBus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="60a36-104">Az.ServiceBus Cmdlets</span></span>
### [<span data-ttu-id="60a36-105">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="60a36-105">Complete-AzServiceBusMigration</span></span>](Complete-AzServiceBusMigration.md)
<span data-ttu-id="60a36-106">Cmdlet 將標準命名空間的移轉設定為完成，標準命名空間的連接字串現在會指向進一步命名空間</span><span class="sxs-lookup"><span data-stu-id="60a36-106">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

### [<span data-ttu-id="60a36-107">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="60a36-107">Get-AzServiceBusAuthorizationRule</span></span>](Get-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="60a36-108">獲得指定命名空間或佇列或主題或 GeoDR 組 (別名的指定授權規則) 。</span><span class="sxs-lookup"><span data-stu-id="60a36-108">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

### [<span data-ttu-id="60a36-109">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="60a36-109">Get-AzServiceBusGeoDRConfiguration</span></span>](Get-AzServiceBusGeoDRConfiguration.md)
<span data-ttu-id="60a36-110">針對主要或 (命名空間，) 復原組選的別名</span><span class="sxs-lookup"><span data-stu-id="60a36-110">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

### [<span data-ttu-id="60a36-111">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="60a36-111">Get-AzServiceBusKey</span></span>](Get-AzServiceBusKey.md)
<span data-ttu-id="60a36-112">在 GeoDR 組配置中，為指定命名空間或佇列或主題或別名 (主要和次要) 。</span><span class="sxs-lookup"><span data-stu-id="60a36-112">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

### [<span data-ttu-id="60a36-113">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="60a36-113">Get-AzServiceBusMigration</span></span>](Get-AzServiceBusMigration.md)
<span data-ttu-id="60a36-114">為命名空間取回 MigrationConfiguration</span><span class="sxs-lookup"><span data-stu-id="60a36-114">Retrieves MigrationConfiguration for the namespace</span></span>

### [<span data-ttu-id="60a36-115">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="60a36-115">Get-AzServiceBusNamespace</span></span>](Get-AzServiceBusNamespace.md)
<span data-ttu-id="60a36-116">在資源群組中，為指定的 Service Bus 命名空間獲得描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-116">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

### [<span data-ttu-id="60a36-117">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="60a36-117">Get-AzServiceBusOperation</span></span>](Get-AzServiceBusOperation.md)
<span data-ttu-id="60a36-118">清單支援的 ServiceBus Operations</span><span class="sxs-lookup"><span data-stu-id="60a36-118">List supported ServiceBus Operations</span></span>

### [<span data-ttu-id="60a36-119">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="60a36-119">Get-AzServiceBusQueue</span></span>](Get-AzServiceBusQueue.md)
<span data-ttu-id="60a36-120">會針對指定的服務母線佇列，返回描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-120">Returns a description for the specified Service Bus queue.</span></span>

### [<span data-ttu-id="60a36-121">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="60a36-121">Get-AzServiceBusRule</span></span>](Get-AzServiceBusRule.md)
<span data-ttu-id="60a36-122">為給定主題訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="60a36-122">Creates a new rule for a given Subscription of Topic.</span></span> 

### [<span data-ttu-id="60a36-123">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="60a36-123">Get-AzServiceBusSubscription</span></span>](Get-AzServiceBusSubscription.md)
<span data-ttu-id="60a36-124">會針對指定的主題，返回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-124">Returns a subscription description for the specified topic.</span></span>

### [<span data-ttu-id="60a36-125">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="60a36-125">Get-AzServiceBusTopic</span></span>](Get-AzServiceBusTopic.md)
<span data-ttu-id="60a36-126">會針對指定的 Service Bus 主題，返回描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-126">Returns a description for the specified Service Bus topic.</span></span>

### [<span data-ttu-id="60a36-127">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="60a36-127">New-AzServiceBusAuthorizationRule</span></span>](New-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="60a36-128">為指定的 Service Bus 指定命名空間或佇列或主題建立新授權規則。</span><span class="sxs-lookup"><span data-stu-id="60a36-128">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

### [<span data-ttu-id="60a36-129">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="60a36-129">New-AzServiceBusAuthorizationRuleSASToken</span></span>](New-AzServiceBusAuthorizationRuleSASToken.md)
<span data-ttu-id="60a36-130">產生 AZURE serviucebus 授權規則的 SAS tolen 命名空間/佇列/topic。</span><span class="sxs-lookup"><span data-stu-id="60a36-130">Generates a SAS tolen for Azure serviucebus authorization rule of namespace/queue/topic.</span></span> 

### [<span data-ttu-id="60a36-131">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="60a36-131">New-AzServiceBusGeoDRConfiguration</span></span>](New-AzServiceBusGeoDRConfiguration.md)
<span data-ttu-id="60a36-132">建立新的別名 (復原組) </span><span class="sxs-lookup"><span data-stu-id="60a36-132">Creates an new Alias(Disaster Recovery configuration)</span></span>

### [<span data-ttu-id="60a36-133">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="60a36-133">New-AzServiceBusKey</span></span>](New-AzServiceBusKey.md)
<span data-ttu-id="60a36-134">重新產生 Service Bus 命名空間或佇列或主題的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="60a36-134">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

### [<span data-ttu-id="60a36-135">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="60a36-135">New-AzServiceBusNamespace</span></span>](New-AzServiceBusNamespace.md)
<span data-ttu-id="60a36-136">建立一個新的 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="60a36-136">Creates a new Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-137">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="60a36-137">New-AzServiceBusQueue</span></span>](New-AzServiceBusQueue.md)
<span data-ttu-id="60a36-138">在指定的 Service Bus 命名空間中建立服務母線佇列。</span><span class="sxs-lookup"><span data-stu-id="60a36-138">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-139">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="60a36-139">New-AzServiceBusRule</span></span>](New-AzServiceBusRule.md)
<span data-ttu-id="60a36-140">為給定主題訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="60a36-140">Creates a new rule for a given Subscription of Topic.</span></span> 

### [<span data-ttu-id="60a36-141">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="60a36-141">New-AzServiceBusSubscription</span></span>](New-AzServiceBusSubscription.md)
<span data-ttu-id="60a36-142">建立指定 Service Bus 主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="60a36-142">Creates a subscription to the specified Service Bus topic.</span></span>

### [<span data-ttu-id="60a36-143">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="60a36-143">New-AzServiceBusTopic</span></span>](New-AzServiceBusTopic.md)
<span data-ttu-id="60a36-144">在指定的 Service Bus 命名空間中建立新 Service Bus 主題。</span><span class="sxs-lookup"><span data-stu-id="60a36-144">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-145">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="60a36-145">Remove-AzServiceBusAuthorizationRule</span></span>](Remove-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="60a36-146">從指定的資源群組移除 Service Bus 命名空間或佇列或主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="60a36-146">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

### [<span data-ttu-id="60a36-147">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="60a36-147">Remove-AzServiceBusGeoDRConfiguration</span></span>](Remove-AzServiceBusGeoDRConfiguration.md)
<span data-ttu-id="60a36-148">刪除復原 (的別名) </span><span class="sxs-lookup"><span data-stu-id="60a36-148">Deletes an Alias(Disaster Recovery configuration)</span></span>

### [<span data-ttu-id="60a36-149">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="60a36-149">Remove-AzServiceBusMigration</span></span>](Remove-AzServiceBusMigration.md)
<span data-ttu-id="60a36-150">Cmdlet 會刪除標準到進一步命名空間的移轉組</span><span class="sxs-lookup"><span data-stu-id="60a36-150">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

### [<span data-ttu-id="60a36-151">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="60a36-151">Remove-AzServiceBusNamespace</span></span>](Remove-AzServiceBusNamespace.md)
<span data-ttu-id="60a36-152">從指定的資源群組移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="60a36-152">Removes the namespace from the specified resource group.</span></span> 

### [<span data-ttu-id="60a36-153">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="60a36-153">Remove-AzServiceBusQueue</span></span>](Remove-AzServiceBusQueue.md)
<span data-ttu-id="60a36-154">從指定的 Service Bus 命名空間移除佇列。</span><span class="sxs-lookup"><span data-stu-id="60a36-154">Removes the queue from the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-155">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="60a36-155">Remove-AzServiceBusRule</span></span>](Remove-AzServiceBusRule.md)
<span data-ttu-id="60a36-156">移除指定訂閱的指定規則。</span><span class="sxs-lookup"><span data-stu-id="60a36-156">Removes the specified rule of a given subscription .</span></span>

### [<span data-ttu-id="60a36-157">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="60a36-157">Remove-AzServiceBusSubscription</span></span>](Remove-AzServiceBusSubscription.md)
<span data-ttu-id="60a36-158">從指定的 Service Bus 命名空間移除主題的訂閱。</span><span class="sxs-lookup"><span data-stu-id="60a36-158">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-159">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="60a36-159">Remove-AzServiceBusTopic</span></span>](Remove-AzServiceBusTopic.md)
<span data-ttu-id="60a36-160">從指定的 Service Bus 命名空間移除主題。</span><span class="sxs-lookup"><span data-stu-id="60a36-160">Removes the topic from the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-161">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="60a36-161">Set-AzServiceBusAuthorizationRule</span></span>](Set-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="60a36-162">更新指定 Service Bus 命名空間或佇列或主題的指定授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-162">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

### [<span data-ttu-id="60a36-163">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="60a36-163">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>](Set-AzServiceBusGeoDRConfigurationBreakPair.md)
<span data-ttu-id="60a36-164">此作業會停用災害復原，並停止從主要命名空間複製到次要命名空間的變更</span><span class="sxs-lookup"><span data-stu-id="60a36-164">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

### [<span data-ttu-id="60a36-165">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="60a36-165">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>](Set-AzServiceBusGeoDRConfigurationFailOver.md)
<span data-ttu-id="60a36-166">會調用 GEO DR 容錯移轉，並重新指定別名以指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="60a36-166">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

### [<span data-ttu-id="60a36-167">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="60a36-167">Set-AzServiceBusNamespace</span></span>](Set-AzServiceBusNamespace.md)
<span data-ttu-id="60a36-168">更新現有 Service Bus 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-168">Updates the description of an existing Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-169">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="60a36-169">Set-AzServiceBusQueue</span></span>](Set-AzServiceBusQueue.md)
<span data-ttu-id="60a36-170">更新指定 Service Bus 命名空間中服務母線佇列的描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-170">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-171">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="60a36-171">Set-AzServiceBusRule</span></span>](Set-AzServiceBusRule.md)
<span data-ttu-id="60a36-172">更新指定訂閱的指定規則描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-172">Updates the specified rule description for the given subscription.</span></span>

### [<span data-ttu-id="60a36-173">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="60a36-173">Set-AzServiceBusSubscription</span></span>](Set-AzServiceBusSubscription.md)
<span data-ttu-id="60a36-174">更新指定 Service Bus 命名空間中 Service Bus 主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-174">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-175">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="60a36-175">Set-AzServiceBusTopic</span></span>](Set-AzServiceBusTopic.md)
<span data-ttu-id="60a36-176">更新指定 Service Bus 命名空間中 Service Bus 主題的描述。</span><span class="sxs-lookup"><span data-stu-id="60a36-176">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="60a36-177">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="60a36-177">Start-AzServiceBusMigration</span></span>](Start-AzServiceBusMigration.md)
<span data-ttu-id="60a36-178">建立新的移移組，並開始將實體從標準命名空間移為進級命名空間</span><span class="sxs-lookup"><span data-stu-id="60a36-178">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

### [<span data-ttu-id="60a36-179">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="60a36-179">Stop-AzServiceBusMigration</span></span>](Stop-AzServiceBusMigration.md)
<span data-ttu-id="60a36-180">{{Fill in The Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="60a36-180">{{Fill in the Synopsis}}</span></span>

### [<span data-ttu-id="60a36-181">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="60a36-181">Test-AzServiceBusName</span></span>](Test-AzServiceBusName.md)
<span data-ttu-id="60a36-182">檢查指定 NameSpace 名稱或別名 (DR 組) </span><span class="sxs-lookup"><span data-stu-id="60a36-182">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

