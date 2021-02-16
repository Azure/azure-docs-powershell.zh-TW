---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: 3101ca2b120860dfa6df95786e235fc88fd0fc78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139362"
---
# <span data-ttu-id="3ffad-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="3ffad-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="3ffad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ffad-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffad-103">取得 CommunicationService 及其屬性。</span><span class="sxs-lookup"><span data-stu-id="3ffad-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="3ffad-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ffad-104">SYNTAX</span></span>

### <span data-ttu-id="3ffad-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="3ffad-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3ffad-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3ffad-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3ffad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3ffad-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ffad-108">List1</span><span class="sxs-lookup"><span data-stu-id="3ffad-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3ffad-109">說明</span><span class="sxs-lookup"><span data-stu-id="3ffad-109">DESCRIPTION</span></span>
<span data-ttu-id="3ffad-110">取得 CommunicationService 及其屬性。</span><span class="sxs-lookup"><span data-stu-id="3ffad-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="3ffad-111">示例</span><span class="sxs-lookup"><span data-stu-id="3ffad-111">EXAMPLES</span></span>

### <span data-ttu-id="3ffad-112">範例1：列出訂閱的現有 CommunicationServices</span><span class="sxs-lookup"><span data-stu-id="3ffad-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="3ffad-113">傳回該訂閱下所有 ACS 資源的清單。</span><span class="sxs-lookup"><span data-stu-id="3ffad-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="3ffad-114">範例2：取得指定 Azure 通訊資源的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3ffad-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="3ffad-115">如果找到一個相符的提供參數，就會傳回 ACS 資源上的資訊。</span><span class="sxs-lookup"><span data-stu-id="3ffad-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="3ffad-116">參數</span><span class="sxs-lookup"><span data-stu-id="3ffad-116">PARAMETERS</span></span>

### <span data-ttu-id="3ffad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffad-117">-DefaultProfile</span></span>
<span data-ttu-id="3ffad-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ffad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ffad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ffad-119">-InputObject</span></span>
<span data-ttu-id="3ffad-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3ffad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ffad-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ffad-121">-Name</span></span>
<span data-ttu-id="3ffad-122">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ffad-122">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="3ffad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ffad-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ffad-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ffad-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ffad-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3ffad-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3ffad-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ffad-126">-SubscriptionId</span></span>
<span data-ttu-id="3ffad-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3ffad-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ffad-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3ffad-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ffad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffad-129">CommonParameters</span></span>
<span data-ttu-id="3ffad-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ffad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffad-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ffad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffad-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3ffad-132">INPUTS</span></span>

### <span data-ttu-id="3ffad-133">ICommunicationIdentity 中的 [Azure. Cmdlet]</span><span class="sxs-lookup"><span data-stu-id="3ffad-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="3ffad-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3ffad-134">OUTPUTS</span></span>

### <span data-ttu-id="3ffad-135">ICommunicationServiceResource 中的 Api20200820Preview （）。</span><span class="sxs-lookup"><span data-stu-id="3ffad-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="3ffad-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3ffad-136">NOTES</span></span>

<span data-ttu-id="3ffad-137">別名</span><span class="sxs-lookup"><span data-stu-id="3ffad-137">ALIASES</span></span>

<span data-ttu-id="3ffad-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3ffad-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ffad-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3ffad-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ffad-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3ffad-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ffad-141">INPUTOBJECT <ICommunicationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3ffad-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ffad-142">`[CommunicationServiceName <String>]`： CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ffad-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="3ffad-143">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3ffad-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ffad-144">`[Location <String>]`： Azure 區域</span><span class="sxs-lookup"><span data-stu-id="3ffad-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="3ffad-145">`[OperationId <String>]`：正在進行中的非同步作業識別碼</span><span class="sxs-lookup"><span data-stu-id="3ffad-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="3ffad-146">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ffad-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3ffad-147">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3ffad-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3ffad-148">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3ffad-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3ffad-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3ffad-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3ffad-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ffad-150">RELATED LINKS</span></span>

