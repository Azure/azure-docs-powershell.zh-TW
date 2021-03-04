---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 17092ab89ded950678e60b079cd30558f7ce2aac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902485"
---
# <span data-ttu-id="37279-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="37279-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="37279-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37279-102">SYNOPSIS</span></span>
<span data-ttu-id="37279-103">從 P2S VpnGateway 獲得目前點至網站連結的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="37279-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="37279-104">語法</span><span class="sxs-lookup"><span data-stu-id="37279-104">SYNTAX</span></span>

### <span data-ttu-id="37279-105">ByP2S VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="37279-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37279-106">ByP2S VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="37279-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37279-107">ByP2S VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="37279-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37279-108">描述</span><span class="sxs-lookup"><span data-stu-id="37279-108">DESCRIPTION</span></span>
<span data-ttu-id="37279-109">**Get-AzP2s VpnGatewayDetailedConnectionHealth** Cmdlet 可讓您從 P2S VpnGateway 取得目前點至網站連結的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="37279-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="37279-110">客戶需要傳遞 SAS URL，我們可以在此輸入詳細的健康情況資訊。</span><span class="sxs-lookup"><span data-stu-id="37279-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="37279-111">例子</span><span class="sxs-lookup"><span data-stu-id="37279-111">EXAMPLES</span></span>

### <span data-ttu-id="37279-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="37279-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="37279-113">**Get-AzP2s VpnGatewayDetailedConnectionHealth** Cmdlet 可讓您從 P2S VpnGateway 取得目前點至網站連結的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="37279-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="37279-114">客戶可以從傳遞的 SAS URL 下載下載健康情況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="37279-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="37279-115">這會顯示每個點到網站連結的資訊，包括使用者名稱、位元組數、位元組數、已配置 IP 位址等。</span><span class="sxs-lookup"><span data-stu-id="37279-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="37279-116">參數</span><span class="sxs-lookup"><span data-stu-id="37279-116">PARAMETERS</span></span>

### <span data-ttu-id="37279-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37279-117">-DefaultProfile</span></span>
<span data-ttu-id="37279-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37279-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37279-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37279-119">-InputObject</span></span>
<span data-ttu-id="37279-120">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="37279-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="37279-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="37279-121">-Name</span></span>
<span data-ttu-id="37279-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="37279-122">The resource name.</span></span>

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

### <span data-ttu-id="37279-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="37279-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="37279-124">p2s vpn 連接健康狀態要寫入的 OutputBlob Sas URL。</span><span class="sxs-lookup"><span data-stu-id="37279-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37279-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37279-125">-ResourceGroupName</span></span>
<span data-ttu-id="37279-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="37279-126">The resource group name.</span></span>

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

### <span data-ttu-id="37279-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37279-127">-ResourceId</span></span>
<span data-ttu-id="37279-128">要修改之 P2S VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="37279-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="37279-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="37279-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="37279-130">要篩選的 P2S vpn 使用者名稱清單。</span><span class="sxs-lookup"><span data-stu-id="37279-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37279-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37279-131">CommonParameters</span></span>
<span data-ttu-id="37279-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37279-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37279-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="37279-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37279-134">輸入</span><span class="sxs-lookup"><span data-stu-id="37279-134">INPUTS</span></span>

### <span data-ttu-id="37279-135">System.String</span><span class="sxs-lookup"><span data-stu-id="37279-135">System.String</span></span>
<span data-ttu-id="37279-136">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37279-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="37279-137">輸出</span><span class="sxs-lookup"><span data-stu-id="37279-137">OUTPUTS</span></span>

### <span data-ttu-id="37279-138">Microsoft.Azure.Commands.Network.models.PSP2S VpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="37279-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="37279-139">筆記</span><span class="sxs-lookup"><span data-stu-id="37279-139">NOTES</span></span>

## <span data-ttu-id="37279-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="37279-140">RELATED LINKS</span></span>
