---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959251"
---
# <span data-ttu-id="a199f-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="a199f-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="a199f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a199f-102">SYNOPSIS</span></span>
<span data-ttu-id="a199f-103">產生並傳回 SAS url 供客戶下載以指向網站用戶端設定的 Vpn 設定檔，以指向 P2SVpnGateway 的網站連線。</span><span class="sxs-lookup"><span data-stu-id="a199f-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="a199f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a199f-104">SYNTAX</span></span>

### <span data-ttu-id="a199f-105">ByP2SVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="a199f-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a199f-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a199f-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a199f-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a199f-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a199f-108">說明</span><span class="sxs-lookup"><span data-stu-id="a199f-108">DESCRIPTION</span></span>
<span data-ttu-id="a199f-109">**AzP2sVpnGatewayVpnProfile** Cmdlet 可讓您產生並取得 SAS url，讓客戶下載指向網站用戶端設定的 Vpn 設定檔，以指向網站連線到 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="a199f-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="a199f-110">使用這個 Vpn 設定檔的 [網站用戶端設定] 只能連線到此特定 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="a199f-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="a199f-111">示例</span><span class="sxs-lookup"><span data-stu-id="a199f-111">EXAMPLES</span></span>

### <span data-ttu-id="a199f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a199f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="a199f-113">**AzP2sVpnGatewayVpnProfile** Cmdlet 可讓您產生並取得 SAS url，讓客戶下載指向網站用戶端設定的 Vpn 設定檔，以指向網站連線到 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="a199f-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="a199f-114">ProfileUrl 會顯示可供客戶下載指向網站用戶端設定之 Vpn 設定檔之位置的 SAS url。</span><span class="sxs-lookup"><span data-stu-id="a199f-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="a199f-115">參數</span><span class="sxs-lookup"><span data-stu-id="a199f-115">PARAMETERS</span></span>

### <span data-ttu-id="a199f-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a199f-116">-AuthenticationMethod</span></span>
<span data-ttu-id="a199f-117">驗證方法</span><span class="sxs-lookup"><span data-stu-id="a199f-117">Authentication Method</span></span>

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

### <span data-ttu-id="a199f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a199f-118">-DefaultProfile</span></span>
<span data-ttu-id="a199f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a199f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a199f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a199f-120">-InputObject</span></span>
<span data-ttu-id="a199f-121">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="a199f-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="a199f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a199f-122">-Name</span></span>
<span data-ttu-id="a199f-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a199f-123">The resource name.</span></span>

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

### <span data-ttu-id="a199f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a199f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a199f-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a199f-125">The resource group name.</span></span>

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

### <span data-ttu-id="a199f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a199f-126">-ResourceId</span></span>
<span data-ttu-id="a199f-127">要修改之 P2SVpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a199f-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="a199f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a199f-128">CommonParameters</span></span>
<span data-ttu-id="a199f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a199f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a199f-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a199f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a199f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a199f-131">INPUTS</span></span>

### <span data-ttu-id="a199f-132">System.object</span><span class="sxs-lookup"><span data-stu-id="a199f-132">System.String</span></span>
<span data-ttu-id="a199f-133">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a199f-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="a199f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a199f-134">OUTPUTS</span></span>

### <span data-ttu-id="a199f-135">PSVpnProfileResponse 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a199f-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="a199f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a199f-136">NOTES</span></span>

## <span data-ttu-id="a199f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a199f-137">RELATED LINKS</span></span>