---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127914"
---
# <span data-ttu-id="c88e3-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="c88e3-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="c88e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c88e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c88e3-103">重新產生 CommunicationService 便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c88e3-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="c88e3-104">PrimaryKey 與 SecondaryKey 無法在同一時間重新產生。</span><span class="sxs-lookup"><span data-stu-id="c88e3-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="c88e3-105">句法</span><span class="sxs-lookup"><span data-stu-id="c88e3-105">SYNTAX</span></span>

### <span data-ttu-id="c88e3-106">RegenerateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="c88e3-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c88e3-107">每當</span><span class="sxs-lookup"><span data-stu-id="c88e3-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c88e3-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c88e3-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c88e3-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c88e3-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c88e3-110">說明</span><span class="sxs-lookup"><span data-stu-id="c88e3-110">DESCRIPTION</span></span>
<span data-ttu-id="c88e3-111">重新產生 CommunicationService 便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c88e3-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="c88e3-112">PrimaryKey 與 SecondaryKey 無法在同一時間重新產生。</span><span class="sxs-lookup"><span data-stu-id="c88e3-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="c88e3-113">示例</span><span class="sxs-lookup"><span data-stu-id="c88e3-113">EXAMPLES</span></span>

### <span data-ttu-id="c88e3-114">範例1：使用 IRegenerateKeyParameters hashtable 重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="c88e3-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="c88e3-115">使上一個主鍵失效、重新產生新的主鍵並傳回它。</span><span class="sxs-lookup"><span data-stu-id="c88e3-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="c88e3-116">範例2：使用 KeyType 來重新產生次要金鑰</span><span class="sxs-lookup"><span data-stu-id="c88e3-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="c88e3-117">使上一個次要金鑰失效、重新產生一個新的金鑰並傳回它。</span><span class="sxs-lookup"><span data-stu-id="c88e3-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="c88e3-118">參數</span><span class="sxs-lookup"><span data-stu-id="c88e3-118">PARAMETERS</span></span>

### <span data-ttu-id="c88e3-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="c88e3-119">-CommunicationServiceName</span></span>
<span data-ttu-id="c88e3-120">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c88e3-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="c88e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88e3-121">-DefaultProfile</span></span>
<span data-ttu-id="c88e3-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c88e3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c88e3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c88e3-123">-InputObject</span></span>
<span data-ttu-id="c88e3-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c88e3-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c88e3-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c88e3-125">-KeyType</span></span>
<span data-ttu-id="c88e3-126">要重新產生的 keyType。</span><span class="sxs-lookup"><span data-stu-id="c88e3-126">The keyType to regenerate.</span></span>
<span data-ttu-id="c88e3-127">必須是 "primary" 或 "次要" (不區分大小寫的) 。</span><span class="sxs-lookup"><span data-stu-id="c88e3-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

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

### <span data-ttu-id="c88e3-128">-參數</span><span class="sxs-lookup"><span data-stu-id="c88e3-128">-Parameter</span></span>
<span data-ttu-id="c88e3-129">參數說明重新產生要構造便捷鍵的要求，請參閱參數屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c88e3-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="c88e3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88e3-130">-ResourceGroupName</span></span>
<span data-ttu-id="c88e3-131">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c88e3-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c88e3-132">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="c88e3-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c88e3-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c88e3-133">-SubscriptionId</span></span>
<span data-ttu-id="c88e3-134">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c88e3-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c88e3-135">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c88e3-135">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c88e3-136">-確認</span><span class="sxs-lookup"><span data-stu-id="c88e3-136">-Confirm</span></span>
<span data-ttu-id="c88e3-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c88e3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c88e3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88e3-138">-WhatIf</span></span>
<span data-ttu-id="c88e3-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c88e3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c88e3-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c88e3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c88e3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88e3-141">CommonParameters</span></span>
<span data-ttu-id="c88e3-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c88e3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88e3-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c88e3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88e3-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c88e3-144">INPUTS</span></span>

### <span data-ttu-id="c88e3-145">IRegenerateKeyParameters 中的 Api20200820Preview （）。</span><span class="sxs-lookup"><span data-stu-id="c88e3-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="c88e3-146">ICommunicationIdentity 中的 [Azure. Cmdlet]</span><span class="sxs-lookup"><span data-stu-id="c88e3-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="c88e3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c88e3-147">OUTPUTS</span></span>

### <span data-ttu-id="c88e3-148">ICommunicationServiceKeys 中的 Api20200820Preview （）。</span><span class="sxs-lookup"><span data-stu-id="c88e3-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="c88e3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c88e3-149">NOTES</span></span>

<span data-ttu-id="c88e3-150">別名</span><span class="sxs-lookup"><span data-stu-id="c88e3-150">ALIASES</span></span>

<span data-ttu-id="c88e3-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c88e3-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c88e3-152">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c88e3-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c88e3-153">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c88e3-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c88e3-154">INPUTOBJECT <ICommunicationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c88e3-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c88e3-155">`[CommunicationServiceName <String>]`： CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c88e3-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="c88e3-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c88e3-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c88e3-157">`[Location <String>]`： Azure 區域</span><span class="sxs-lookup"><span data-stu-id="c88e3-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="c88e3-158">`[OperationId <String>]`：正在進行中的非同步作業識別碼</span><span class="sxs-lookup"><span data-stu-id="c88e3-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="c88e3-159">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c88e3-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c88e3-160">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="c88e3-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c88e3-161">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c88e3-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c88e3-162">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c88e3-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="c88e3-163">參數 <IRegenerateKeyParameters> ：參數描述重新產生便捷鍵的要求</span><span class="sxs-lookup"><span data-stu-id="c88e3-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="c88e3-164">`[KeyType <KeyType?>]`：要重新產生的 keyType。</span><span class="sxs-lookup"><span data-stu-id="c88e3-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="c88e3-165">必須是 "primary" 或 "次要" (不區分大小寫的) 。</span><span class="sxs-lookup"><span data-stu-id="c88e3-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="c88e3-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="c88e3-166">RELATED LINKS</span></span>

