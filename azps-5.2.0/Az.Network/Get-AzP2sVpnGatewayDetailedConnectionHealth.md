---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284584"
---
# <span data-ttu-id="9ead5-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="9ead5-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="9ead5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ead5-102">SYNOPSIS</span></span>
<span data-ttu-id="9ead5-103">從 P2SVpnGateway 取得目前指向網站連線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9ead5-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="9ead5-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ead5-104">SYNTAX</span></span>

### <span data-ttu-id="9ead5-105">ByP2SVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="9ead5-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ead5-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9ead5-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ead5-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9ead5-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ead5-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ead5-108">DESCRIPTION</span></span>
<span data-ttu-id="9ead5-109">**AzP2sVpnGatewayDetailedConnectionHealth** Cmdlet 可讓您從 P2SVpnGateway 取得目前指向網站連線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9ead5-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="9ead5-110">客戶需要傳送 SAS url，讓我們可以將這些詳細的健康資訊放在其中。</span><span class="sxs-lookup"><span data-stu-id="9ead5-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="9ead5-111">示例</span><span class="sxs-lookup"><span data-stu-id="9ead5-111">EXAMPLES</span></span>

### <span data-ttu-id="9ead5-112">範例1</span><span class="sxs-lookup"><span data-stu-id="9ead5-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="9ead5-113">**AzP2sVpnGatewayDetailedConnectionHealth** Cmdlet 可讓您從 P2SVpnGateway 取得目前指向網站連線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9ead5-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="9ead5-114">客戶可以從已傳送的 SAS url 下載下載健康情況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ead5-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="9ead5-115">這會顯示每個網站連線與使用者名、位元組數、位元組數、已分配 ip 位址等相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="9ead5-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="9ead5-116">參數</span><span class="sxs-lookup"><span data-stu-id="9ead5-116">PARAMETERS</span></span>

### <span data-ttu-id="9ead5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ead5-117">-DefaultProfile</span></span>
<span data-ttu-id="9ead5-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ead5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ead5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ead5-119">-InputObject</span></span>
<span data-ttu-id="9ead5-120">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="9ead5-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="9ead5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ead5-121">-Name</span></span>
<span data-ttu-id="9ead5-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9ead5-122">The resource name.</span></span>

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

### <span data-ttu-id="9ead5-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="9ead5-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="9ead5-124">P2s vpn 連線健康情況將寫入的 OutputBlob Sas url。</span><span class="sxs-lookup"><span data-stu-id="9ead5-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="9ead5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ead5-125">-ResourceGroupName</span></span>
<span data-ttu-id="9ead5-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ead5-126">The resource group name.</span></span>

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

### <span data-ttu-id="9ead5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ead5-127">-ResourceId</span></span>
<span data-ttu-id="9ead5-128">要修改之 P2SVpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ead5-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="9ead5-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="9ead5-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="9ead5-130">要篩選的 P2S vpn 使用者名稱清單。</span><span class="sxs-lookup"><span data-stu-id="9ead5-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="9ead5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ead5-131">CommonParameters</span></span>
<span data-ttu-id="9ead5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ead5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ead5-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ead5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ead5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9ead5-134">INPUTS</span></span>

### <span data-ttu-id="9ead5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="9ead5-135">System.String</span></span>
<span data-ttu-id="9ead5-136">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ead5-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="9ead5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9ead5-137">OUTPUTS</span></span>

### <span data-ttu-id="9ead5-138">PSP2SVpnConnectionHealth 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ead5-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="9ead5-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9ead5-139">NOTES</span></span>

## <span data-ttu-id="9ead5-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ead5-140">RELATED LINKS</span></span>
