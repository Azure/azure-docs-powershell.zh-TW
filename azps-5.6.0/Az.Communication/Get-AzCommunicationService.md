---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: f9f4cc86a07c50718511c3ed0889d96f7acec9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912101"
---
# <span data-ttu-id="e119a-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="e119a-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="e119a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e119a-102">SYNOPSIS</span></span>
<span data-ttu-id="e119a-103">取得 CommunicationService 及其屬性。</span><span class="sxs-lookup"><span data-stu-id="e119a-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="e119a-104">語法</span><span class="sxs-lookup"><span data-stu-id="e119a-104">SYNTAX</span></span>

### <span data-ttu-id="e119a-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="e119a-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e119a-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e119a-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e119a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e119a-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e119a-108">清單1</span><span class="sxs-lookup"><span data-stu-id="e119a-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e119a-109">描述</span><span class="sxs-lookup"><span data-stu-id="e119a-109">DESCRIPTION</span></span>
<span data-ttu-id="e119a-110">取得 CommunicationService 及其屬性。</span><span class="sxs-lookup"><span data-stu-id="e119a-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="e119a-111">例子</span><span class="sxs-lookup"><span data-stu-id="e119a-111">EXAMPLES</span></span>

### <span data-ttu-id="e119a-112">範例 1：列出訂閱的現有 CommunicationServices</span><span class="sxs-lookup"><span data-stu-id="e119a-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="e119a-113">會返回該訂閱下的所有 ACS 資源清單。</span><span class="sxs-lookup"><span data-stu-id="e119a-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="e119a-114">範例 2：取得指定 Azure 通訊資源的資訊</span><span class="sxs-lookup"><span data-stu-id="e119a-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="e119a-115">如果找到一個符合所提供的參數，則會返回 ACS 資源上的資訊。</span><span class="sxs-lookup"><span data-stu-id="e119a-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="e119a-116">參數</span><span class="sxs-lookup"><span data-stu-id="e119a-116">PARAMETERS</span></span>

### <span data-ttu-id="e119a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e119a-117">-DefaultProfile</span></span>
<span data-ttu-id="e119a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e119a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e119a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e119a-119">-InputObject</span></span>
<span data-ttu-id="e119a-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e119a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e119a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e119a-121">-Name</span></span>
<span data-ttu-id="e119a-122">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e119a-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e119a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e119a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e119a-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e119a-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e119a-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e119a-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e119a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e119a-126">-SubscriptionId</span></span>
<span data-ttu-id="e119a-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e119a-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e119a-128">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e119a-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e119a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e119a-129">CommonParameters</span></span>
<span data-ttu-id="e119a-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e119a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e119a-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e119a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e119a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e119a-132">INPUTS</span></span>

### <span data-ttu-id="e119a-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="e119a-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="e119a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e119a-134">OUTPUTS</span></span>

### <span data-ttu-id="e119a-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="e119a-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="e119a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e119a-136">NOTES</span></span>

<span data-ttu-id="e119a-137">別名</span><span class="sxs-lookup"><span data-stu-id="e119a-137">ALIASES</span></span>

<span data-ttu-id="e119a-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e119a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e119a-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e119a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e119a-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e119a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e119a-141">INPUTOBJECT： <ICommunicationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e119a-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e119a-142">`[CommunicationServiceName <String>]`：CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e119a-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="e119a-143">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e119a-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e119a-144">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="e119a-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="e119a-145">`[OperationId <String>]`：進行中的同步作業識別碼</span><span class="sxs-lookup"><span data-stu-id="e119a-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="e119a-146">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e119a-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e119a-147">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e119a-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e119a-148">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e119a-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e119a-149">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e119a-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e119a-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e119a-150">RELATED LINKS</span></span>

