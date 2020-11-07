---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/get-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: 5523dd35ae91b9fea7db5f2451401793cb6059c2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966711"
---
# <span data-ttu-id="f6182-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="f6182-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="f6182-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6182-102">SYNOPSIS</span></span>
<span data-ttu-id="f6182-103">取得特定的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="f6182-103">Get a specific gallery item.</span></span>

## <span data-ttu-id="f6182-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6182-104">SYNTAX</span></span>

### <span data-ttu-id="f6182-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f6182-105">List (Default)</span></span>
```
Get-AzsGalleryItem [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6182-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f6182-106">Get</span></span>
```
Get-AzsGalleryItem -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="f6182-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6182-107">GetViaIdentity</span></span>
```
Get-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f6182-108">說明</span><span class="sxs-lookup"><span data-stu-id="f6182-108">DESCRIPTION</span></span>
<span data-ttu-id="f6182-109">取得特定的圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="f6182-109">Get a specific gallery item.</span></span>

## <span data-ttu-id="f6182-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6182-110">EXAMPLES</span></span>

### <span data-ttu-id="f6182-111">範例1： Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="f6182-111">Example 1: Get-AzsGalleryItem</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM
```

<span data-ttu-id="f6182-112">依名稱取得圖庫專案。</span><span class="sxs-lookup"><span data-stu-id="f6182-112">Gets the gallery item by name.</span></span>

### <span data-ttu-id="f6182-113">範例2：清單庫專案</span><span class="sxs-lookup"><span data-stu-id="f6182-113">Example 2: List Gallery Items</span></span>
```powershell
PS C:\> Get-AzsGalleryItem

Name                                       Publisher PublisherDisplayName  ItemName                  ItemDisplayName
----                                       --------- --------------------  --------                  ---------------
Canonical.UbuntuServer1804LTS-ARM.1.0.3    Canonical Canonical             UbuntuServer1804LTS-ARM   Ubuntu Server 1...
Microsoft.AddOnRP-WindowsServer.1.1910.3   Microsoft Microsoft             AddOnRP-WindowsServer     Microsoft Azure...
Microsoft.AdminOffer.6.0.0                 Microsoft Microsoft Corporation AdminOffer                Offer
Microsoft.AvailabilitySet-ARM.1.0.1        Microsoft Microsoft             AvailabilitySet-ARM       Availability Set
Microsoft.Connection-ARM.1.2.2             Microsoft Microsoft             Connection-ARM            Connection
Microsoft.CustomScriptExtension-arm.2.0.10 Microsoft Microsoft Corp.       CustomScriptExtension-arm Custom Script E...
Microsoft.DSC-arm.2.0.7                    Microsoft Microsoft Corp.       DSC-arm                   PowerShell Desi...
Microsoft.DnsZone-ARM.1.0.1                Microsoft Microsoft             DnsZone-ARM               DNS zone
Microsoft.Image-ARM.1.0.2                  Microsoft Microsoft             Image-ARM                 Image
Microsoft.KeyVault.1.0.14                  Microsoft Microsoft             KeyVault                  Key Vault
Microsoft.LoadBalancer-ARM.1.0.2           Microsoft Microsoft             LoadBalancer-ARM          Load Balancer
Microsoft.LocalNetworkGateway-ARM.1.0.3    Microsoft Microsoft             LocalNetworkGateway-ARM   Local network g...
Microsoft.ManagedDisk-ARM.1.0.2            Microsoft Microsoft             ManagedDisk-ARM           Managed Disks
Microsoft.NetworkInterface-ARM.1.0.4       Microsoft Microsoft             NetworkInterface-ARM      Network interface
Microsoft.NetworkSecurityGroup-ARM.1.0.4   Microsoft Microsoft             NetworkSecurityGroup-ARM  Network securit...
Microsoft.Offer.6.0.0                      Microsoft Microsoft Corporation Offer                     Offer
Microsoft.Plan.6.0.0                       Microsoft Microsoft Corporation Plan                      Plan
Microsoft.PublicIPAddress-ARM.1.0.2        Microsoft Microsoft             PublicIPAddress-ARM       Public IP address
Microsoft.PublicIPPool-ARM.1.0.0           Microsoft Microsoft             PublicIPPool-ARM          Public IP pool
Microsoft.ResourceGroup.6.0.0              Microsoft Microsoft             ResourceGroup             Resource group
Microsoft.RouteTable-ARM.1.0.2             Microsoft Microsoft             RouteTable-ARM            Route table
Microsoft.ScaleUnitNode-ARM.1.0.0          Microsoft Microsoft             ScaleUnitNode-ARM         Scale Unit Node
Microsoft.Snapshot-ARM.1.0.2               Microsoft Microsoft             Snapshot-ARM              Snapshot
Microsoft.StorageAccount-ARM.101.0.1       Microsoft Microsoft             StorageAccount-ARM        Storage account
Microsoft.StorageAccount-ARM.1.0.3         Microsoft Microsoft             StorageAccount-ARM        Storage account...
Microsoft.Template.6.0.0                   Microsoft Microsoft             Template                  Template deploy...
Microsoft.TenantSubscription.6.0.0         Microsoft Microsoft Corporation TenantSubscription        Subscription
Microsoft.VirtualMachine-ARM.1.0.2         Microsoft Microsoft             VirtualMachine-ARM        Virtual machine
Microsoft.VirtualNetwork-ARM.1.0.4         Microsoft Microsoft             VirtualNetwork-ARM        Virtual network
Microsoft.VirtualNetworkGateway-ARM.1.0.3  Microsoft Microsoft             VirtualNetworkGateway-ARM Virtual network...
microsoft.antimalware-windows-arm.1.0.0    microsoft Microsoft Corp.       antimalware-windows-arm   Microsoft Antim...
microsoft.custom-script2-linux-arm.3.0.0   microsoft Microsoft Corp.       custom-script2-linux-arm  Custom Script F...
microsoft.custom-script-linux-arm.2.0.50   microsoft Microsoft Corp.       custom-script-linux-arm   Custom Script F...
microsoft.docker-arm.1.1.0                 microsoft Microsoft             docker-arm                Docker
microsoft.vmss.7.1.7                       microsoft Microsoft             vmss                      Virtual machine...

```

<span data-ttu-id="f6182-114">列出 Azure 堆疊圖庫中所有可用的專案。</span><span class="sxs-lookup"><span data-stu-id="f6182-114">Lists all the items available in the Azure Stack gallery.</span></span>

## <span data-ttu-id="f6182-115">參數</span><span class="sxs-lookup"><span data-stu-id="f6182-115">PARAMETERS</span></span>

### <span data-ttu-id="f6182-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6182-116">-DefaultProfile</span></span>
<span data-ttu-id="f6182-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6182-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6182-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6182-118">-InputObject</span></span>
<span data-ttu-id="f6182-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6182-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f6182-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6182-120">-Name</span></span>
<span data-ttu-id="f6182-121">圖庫專案的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f6182-121">Identity of the gallery item.</span></span>
<span data-ttu-id="f6182-122">包括發行者名稱、專案名稱，並且可能包含以句點字元分隔的版本。</span><span class="sxs-lookup"><span data-stu-id="f6182-122">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f6182-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6182-123">-PassThru</span></span>
<span data-ttu-id="f6182-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="f6182-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f6182-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6182-125">-SubscriptionId</span></span>
<span data-ttu-id="f6182-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f6182-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6182-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f6182-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f6182-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6182-128">CommonParameters</span></span>
<span data-ttu-id="f6182-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6182-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6182-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6182-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6182-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f6182-131">INPUTS</span></span>

### <span data-ttu-id="f6182-132">[IGalleryIdentity] 的圖庫。</span><span class="sxs-lookup"><span data-stu-id="f6182-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="f6182-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f6182-133">OUTPUTS</span></span>

### <span data-ttu-id="f6182-134">IGalleryItem 中的 [Api20150401] 樣式。</span><span class="sxs-lookup"><span data-stu-id="f6182-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="f6182-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f6182-135">NOTES</span></span>

<span data-ttu-id="f6182-136">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f6182-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6182-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f6182-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f6182-138">INPUTOBJECT <IGalleryIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f6182-138">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6182-139">`[GalleryItemName <String>]`：圖庫專案的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f6182-139">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="f6182-140">包括發行者名稱、專案名稱，並且可能包含以句點字元分隔的版本。</span><span class="sxs-lookup"><span data-stu-id="f6182-140">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="f6182-141">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f6182-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6182-142">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f6182-142">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f6182-143">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f6182-143">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f6182-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6182-144">RELATED LINKS</span></span>

