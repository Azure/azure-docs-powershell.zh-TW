---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794874"
---
# <span data-ttu-id="b03fd-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="b03fd-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="b03fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b03fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b03fd-103">取得網路資源提供者狀態的概覽。</span><span class="sxs-lookup"><span data-stu-id="b03fd-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="b03fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="b03fd-104">SYNTAX</span></span>

### <span data-ttu-id="b03fd-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="b03fd-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b03fd-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b03fd-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b03fd-107">說明</span><span class="sxs-lookup"><span data-stu-id="b03fd-107">DESCRIPTION</span></span>
<span data-ttu-id="b03fd-108">取得網路資源提供者狀態的概覽。</span><span class="sxs-lookup"><span data-stu-id="b03fd-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="b03fd-109">示例</span><span class="sxs-lookup"><span data-stu-id="b03fd-109">EXAMPLES</span></span>

### <span data-ttu-id="b03fd-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b03fd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="b03fd-111">參數</span><span class="sxs-lookup"><span data-stu-id="b03fd-111">PARAMETERS</span></span>

### <span data-ttu-id="b03fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03fd-112">-DefaultProfile</span></span>
<span data-ttu-id="b03fd-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b03fd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03fd-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b03fd-114">-InputObject</span></span>
<span data-ttu-id="b03fd-115">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b03fd-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b03fd-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b03fd-116">-SubscriptionId</span></span>
<span data-ttu-id="b03fd-117">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b03fd-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b03fd-118">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b03fd-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b03fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03fd-119">CommonParameters</span></span>
<span data-ttu-id="b03fd-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b03fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03fd-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b03fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03fd-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b03fd-122">INPUTS</span></span>

### <span data-ttu-id="b03fd-123">INetworkAdminIdentity （NetworkAdmin）的</span><span class="sxs-lookup"><span data-stu-id="b03fd-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="b03fd-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b03fd-124">OUTPUTS</span></span>

### <span data-ttu-id="b03fd-125">IAdminOverview （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="b03fd-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="b03fd-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b03fd-126">NOTES</span></span>

<span data-ttu-id="b03fd-127">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b03fd-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b03fd-128">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b03fd-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b03fd-129">INPUTOBJECT <INetworkAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b03fd-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b03fd-130">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b03fd-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b03fd-131">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b03fd-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b03fd-132">`[ResourceName <String>]`：資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b03fd-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="b03fd-133">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b03fd-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b03fd-134">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b03fd-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b03fd-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b03fd-135">RELATED LINKS</span></span>

