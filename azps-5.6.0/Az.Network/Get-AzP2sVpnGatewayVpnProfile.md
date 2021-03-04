---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: e606f961cf54eb390e76e3f9bc8c00e556aff7fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902482"
---
# <span data-ttu-id="ea930-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="ea930-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="ea930-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea930-102">SYNOPSIS</span></span>
<span data-ttu-id="ea930-103">產生並返回一個 SAS URL，供客戶下載 Vpn 設定檔，讓指向網站用戶端設定具有指向 P2S VpnGateway 的網站連接。</span><span class="sxs-lookup"><span data-stu-id="ea930-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="ea930-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea930-104">SYNTAX</span></span>

### <span data-ttu-id="ea930-105">ByP2S VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="ea930-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea930-106">ByP2S VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ea930-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea930-107">ByP2S VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ea930-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea930-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea930-108">DESCRIPTION</span></span>
<span data-ttu-id="ea930-109">**Get-AzP2s VpnGateway VpnProfile** Cmdlet 可讓您產生並取得客戶下載 VPN 設定檔的 SAS URL，以指向網站用戶端設定，以指向 P2S VpnGateway 的網站連接。</span><span class="sxs-lookup"><span data-stu-id="ea930-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="ea930-110">使用此 Vpn 設定檔指向網站用戶端設定，只能連接到這個特定的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="ea930-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="ea930-111">例子</span><span class="sxs-lookup"><span data-stu-id="ea930-111">EXAMPLES</span></span>

### <span data-ttu-id="ea930-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="ea930-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="ea930-113">**Get-AzP2s VpnGateway VpnProfile** Cmdlet 可讓您產生並取得客戶下載 VPN 設定檔的 SAS URL，以指向網站用戶端設定，以指向 P2S VpnGateway 的網站連接。</span><span class="sxs-lookup"><span data-stu-id="ea930-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="ea930-114">ProfileUrl 會顯示 SAS URL，客戶可從其中下載指向網站用戶端設定之 Vpn 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea930-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="ea930-115">參數</span><span class="sxs-lookup"><span data-stu-id="ea930-115">PARAMETERS</span></span>

### <span data-ttu-id="ea930-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ea930-116">-AuthenticationMethod</span></span>
<span data-ttu-id="ea930-117">驗證方法</span><span class="sxs-lookup"><span data-stu-id="ea930-117">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea930-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea930-118">-DefaultProfile</span></span>
<span data-ttu-id="ea930-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea930-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea930-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea930-120">-InputObject</span></span>
<span data-ttu-id="ea930-121">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="ea930-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea930-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea930-122">-Name</span></span>
<span data-ttu-id="ea930-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ea930-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea930-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea930-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea930-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ea930-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea930-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea930-126">-ResourceId</span></span>
<span data-ttu-id="ea930-127">要修改之 P2S VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea930-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea930-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea930-128">CommonParameters</span></span>
<span data-ttu-id="ea930-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea930-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea930-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ea930-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea930-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ea930-131">INPUTS</span></span>

### <span data-ttu-id="ea930-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ea930-132">System.String</span></span>
<span data-ttu-id="ea930-133">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="ea930-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="ea930-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ea930-134">OUTPUTS</span></span>

### <span data-ttu-id="ea930-135">Microsoft.Azure.Commands.Network.models.PS VpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="ea930-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="ea930-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ea930-136">NOTES</span></span>

## <span data-ttu-id="ea930-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea930-137">RELATED LINKS</span></span>
