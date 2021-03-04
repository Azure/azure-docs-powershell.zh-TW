---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: 4b9186265287c52c27cff6cb1a7f0d0570949e76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912085"
---
# <span data-ttu-id="439c8-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="439c8-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="439c8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="439c8-102">SYNOPSIS</span></span>
<span data-ttu-id="439c8-103">重新產生 CommunicationService 便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="439c8-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="439c8-104">PrimaryKey 和 SecondaryKey 無法同時重新產生。</span><span class="sxs-lookup"><span data-stu-id="439c8-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="439c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="439c8-105">SYNTAX</span></span>

### <span data-ttu-id="439c8-106">重新產生Expanded (預設) </span><span class="sxs-lookup"><span data-stu-id="439c8-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="439c8-107">再生</span><span class="sxs-lookup"><span data-stu-id="439c8-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="439c8-108">重新產生ViaIdentity</span><span class="sxs-lookup"><span data-stu-id="439c8-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="439c8-109">重新產生ViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="439c8-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="439c8-110">描述</span><span class="sxs-lookup"><span data-stu-id="439c8-110">DESCRIPTION</span></span>
<span data-ttu-id="439c8-111">重新產生 CommunicationService 便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="439c8-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="439c8-112">PrimaryKey 和 SecondaryKey 無法同時重新產生。</span><span class="sxs-lookup"><span data-stu-id="439c8-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="439c8-113">例子</span><span class="sxs-lookup"><span data-stu-id="439c8-113">EXAMPLES</span></span>

### <span data-ttu-id="439c8-114">範例 1：使用 IRegenerateKeyParameters 雜湊表重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="439c8-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="439c8-115">將上一個主鍵失效，重新產生新主鍵並返回。</span><span class="sxs-lookup"><span data-stu-id="439c8-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="439c8-116">範例 2：使用 KeyType 重新產生次要金鑰</span><span class="sxs-lookup"><span data-stu-id="439c8-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="439c8-117">將上一個次要金鑰失效，重新產生新金鑰並返回。</span><span class="sxs-lookup"><span data-stu-id="439c8-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="439c8-118">參數</span><span class="sxs-lookup"><span data-stu-id="439c8-118">PARAMETERS</span></span>

### <span data-ttu-id="439c8-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="439c8-119">-CommunicationServiceName</span></span>
<span data-ttu-id="439c8-120">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="439c8-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439c8-121">-DefaultProfile</span></span>
<span data-ttu-id="439c8-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="439c8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="439c8-123">-InputObject</span></span>
<span data-ttu-id="439c8-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="439c8-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="439c8-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="439c8-125">-KeyType</span></span>
<span data-ttu-id="439c8-126">要重新產生之 KeyType。</span><span class="sxs-lookup"><span data-stu-id="439c8-126">The keyType to regenerate.</span></span>
<span data-ttu-id="439c8-127">必須是'主要'或'次要' (區分大小寫) 。</span><span class="sxs-lookup"><span data-stu-id="439c8-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c8-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="439c8-128">-Parameter</span></span>
<span data-ttu-id="439c8-129">參數描述重新產生便捷鍵的要求：若要建構，請參閱 PARAMETER 屬性的 NOTES 區段，以及建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="439c8-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="439c8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439c8-130">-ResourceGroupName</span></span>
<span data-ttu-id="439c8-131">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="439c8-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="439c8-132">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="439c8-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c8-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="439c8-133">-SubscriptionId</span></span>
<span data-ttu-id="439c8-134">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="439c8-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="439c8-135">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="439c8-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439c8-136">-確認</span><span class="sxs-lookup"><span data-stu-id="439c8-136">-Confirm</span></span>
<span data-ttu-id="439c8-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="439c8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="439c8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439c8-138">-WhatIf</span></span>
<span data-ttu-id="439c8-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="439c8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="439c8-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="439c8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="439c8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439c8-141">CommonParameters</span></span>
<span data-ttu-id="439c8-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="439c8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439c8-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="439c8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439c8-144">輸入</span><span class="sxs-lookup"><span data-stu-id="439c8-144">INPUTS</span></span>

### <span data-ttu-id="439c8-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="439c8-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="439c8-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="439c8-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="439c8-147">輸出</span><span class="sxs-lookup"><span data-stu-id="439c8-147">OUTPUTS</span></span>

### <span data-ttu-id="439c8-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="439c8-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="439c8-149">筆記</span><span class="sxs-lookup"><span data-stu-id="439c8-149">NOTES</span></span>

<span data-ttu-id="439c8-150">別名</span><span class="sxs-lookup"><span data-stu-id="439c8-150">ALIASES</span></span>

<span data-ttu-id="439c8-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="439c8-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="439c8-152">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="439c8-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="439c8-153">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="439c8-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="439c8-154">INPUTOBJECT： <ICommunicationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="439c8-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="439c8-155">`[CommunicationServiceName <String>]`：CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="439c8-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="439c8-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="439c8-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="439c8-157">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="439c8-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="439c8-158">`[OperationId <String>]`：進行中的同步作業識別碼</span><span class="sxs-lookup"><span data-stu-id="439c8-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="439c8-159">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="439c8-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="439c8-160">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="439c8-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="439c8-161">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="439c8-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="439c8-162">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="439c8-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="439c8-163">PARAMETER <IRegenerateKeyParameters> ：參數描述重新產生便捷鍵的要求</span><span class="sxs-lookup"><span data-stu-id="439c8-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="439c8-164">`[KeyType <KeyType?>]`：要重新產生之 KeyType。</span><span class="sxs-lookup"><span data-stu-id="439c8-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="439c8-165">必須是'主要'或'次要' (區分大小寫) 。</span><span class="sxs-lookup"><span data-stu-id="439c8-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="439c8-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="439c8-166">RELATED LINKS</span></span>

