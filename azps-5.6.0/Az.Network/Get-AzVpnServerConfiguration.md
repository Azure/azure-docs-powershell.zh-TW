---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 0d669aca3eaf330322ff814f51bd0c412400f457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905345"
---
# <span data-ttu-id="3c907-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c907-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="3c907-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c907-102">SYNOPSIS</span></span>
<span data-ttu-id="3c907-103">獲得指向網站連接的現有 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="3c907-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="3c907-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c907-104">SYNTAX</span></span>

### <span data-ttu-id="3c907-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="3c907-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c907-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c907-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c907-107">描述</span><span class="sxs-lookup"><span data-stu-id="3c907-107">DESCRIPTION</span></span>
<span data-ttu-id="3c907-108">**Get-Az VpnServerConfiguration** Cmdlet 會針對指向網站連線性，會返回現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="3c907-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="3c907-109">例子</span><span class="sxs-lookup"><span data-stu-id="3c907-109">EXAMPLES</span></span>

### <span data-ttu-id="3c907-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3c907-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="3c907-111">上述命令會取得現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="3c907-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="3c907-112">參數</span><span class="sxs-lookup"><span data-stu-id="3c907-112">PARAMETERS</span></span>

### <span data-ttu-id="3c907-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c907-113">-DefaultProfile</span></span>
<span data-ttu-id="3c907-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c907-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c907-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c907-115">-Name</span></span>
<span data-ttu-id="3c907-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3c907-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c907-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c907-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c907-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3c907-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c907-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c907-119">CommonParameters</span></span>
<span data-ttu-id="3c907-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c907-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c907-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3c907-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c907-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3c907-122">INPUTS</span></span>

### <span data-ttu-id="3c907-123">沒有</span><span class="sxs-lookup"><span data-stu-id="3c907-123">None</span></span>

## <span data-ttu-id="3c907-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3c907-124">OUTPUTS</span></span>

### <span data-ttu-id="3c907-125">Microsoft.Azure.Commands.Network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c907-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="3c907-126">筆記</span><span class="sxs-lookup"><span data-stu-id="3c907-126">NOTES</span></span>

## <span data-ttu-id="3c907-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c907-127">RELATED LINKS</span></span>
