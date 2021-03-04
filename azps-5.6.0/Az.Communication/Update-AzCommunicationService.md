---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 53127b970c3c2f588a54eaec3dcd9ea1174a7053
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912073"
---
# <span data-ttu-id="6d325-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="6d325-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="6d325-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6d325-102">SYNOPSIS</span></span>
<span data-ttu-id="6d325-103">更新現有 CommunicationService 的作業。</span><span class="sxs-lookup"><span data-stu-id="6d325-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="6d325-104">語法</span><span class="sxs-lookup"><span data-stu-id="6d325-104">SYNTAX</span></span>

### <span data-ttu-id="6d325-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6d325-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d325-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6d325-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d325-107">描述</span><span class="sxs-lookup"><span data-stu-id="6d325-107">DESCRIPTION</span></span>
<span data-ttu-id="6d325-108">更新現有 CommunicationService 的作業。</span><span class="sxs-lookup"><span data-stu-id="6d325-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="6d325-109">例子</span><span class="sxs-lookup"><span data-stu-id="6d325-109">EXAMPLES</span></span>

### <span data-ttu-id="6d325-110">範例 1：將現有的 ACS 資源更新為具有標記</span><span class="sxs-lookup"><span data-stu-id="6d325-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="6d325-111">將指定的標記附加到指定的 ACS 資源。</span><span class="sxs-lookup"><span data-stu-id="6d325-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="6d325-112">參數</span><span class="sxs-lookup"><span data-stu-id="6d325-112">PARAMETERS</span></span>

### <span data-ttu-id="6d325-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d325-113">-DefaultProfile</span></span>
<span data-ttu-id="6d325-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d325-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d325-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d325-115">-InputObject</span></span>
<span data-ttu-id="6d325-116">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6d325-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d325-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d325-117">-Name</span></span>
<span data-ttu-id="6d325-118">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d325-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d325-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d325-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d325-120">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6d325-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d325-121">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6d325-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d325-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d325-122">-SubscriptionId</span></span>
<span data-ttu-id="6d325-123">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d325-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d325-124">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6d325-124">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d325-125">-標記</span><span class="sxs-lookup"><span data-stu-id="6d325-125">-Tag</span></span>
<span data-ttu-id="6d325-126">服務標記，這是描述資源的金鑰值組清單。</span><span class="sxs-lookup"><span data-stu-id="6d325-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d325-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6d325-127">-Confirm</span></span>
<span data-ttu-id="6d325-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6d325-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d325-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d325-129">-WhatIf</span></span>
<span data-ttu-id="6d325-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d325-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d325-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d325-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d325-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d325-132">CommonParameters</span></span>
<span data-ttu-id="6d325-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6d325-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d325-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d325-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d325-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6d325-135">INPUTS</span></span>

### <span data-ttu-id="6d325-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="6d325-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="6d325-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6d325-137">OUTPUTS</span></span>

### <span data-ttu-id="6d325-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="6d325-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="6d325-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6d325-139">NOTES</span></span>

<span data-ttu-id="6d325-140">別名</span><span class="sxs-lookup"><span data-stu-id="6d325-140">ALIASES</span></span>

<span data-ttu-id="6d325-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6d325-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d325-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6d325-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d325-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6d325-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d325-144">INPUTOBJECT： <ICommunicationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6d325-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d325-145">`[CommunicationServiceName <String>]`：CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d325-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="6d325-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6d325-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d325-147">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="6d325-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="6d325-148">`[OperationId <String>]`：進行中的同步作業識別碼</span><span class="sxs-lookup"><span data-stu-id="6d325-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="6d325-149">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6d325-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6d325-150">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6d325-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6d325-151">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d325-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="6d325-152">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6d325-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d325-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d325-153">RELATED LINKS</span></span>

