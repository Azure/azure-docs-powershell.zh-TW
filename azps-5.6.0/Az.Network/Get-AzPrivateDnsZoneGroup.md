---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: f9428c2249cf69d366a6770d448e82618d98896f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902481"
---
# <span data-ttu-id="99b44-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="99b44-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="99b44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="99b44-102">SYNOPSIS</span></span>
<span data-ttu-id="99b44-103">獲得私人 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="99b44-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="99b44-104">語法</span><span class="sxs-lookup"><span data-stu-id="99b44-104">SYNTAX</span></span>

### <span data-ttu-id="99b44-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="99b44-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b44-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="99b44-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b44-107">描述</span><span class="sxs-lookup"><span data-stu-id="99b44-107">DESCRIPTION</span></span>
<span data-ttu-id="99b44-108">**Get-AzPrivateDnsZoneGroup Cmdlet** 會取得一或多個私人 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="99b44-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="99b44-109">例子</span><span class="sxs-lookup"><span data-stu-id="99b44-109">EXAMPLES</span></span>

### <span data-ttu-id="99b44-110">範例 1：取回私人 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="99b44-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="99b44-111">上述範例會獲得資源群組 rg 中名為 dnsgroup1 的私人 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="99b44-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="99b44-112">參數</span><span class="sxs-lookup"><span data-stu-id="99b44-112">PARAMETERS</span></span>

### <span data-ttu-id="99b44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b44-113">-DefaultProfile</span></span>
<span data-ttu-id="99b44-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="99b44-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b44-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="99b44-115">-Name</span></span>
<span data-ttu-id="99b44-116">私人 dns 區域組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99b44-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b44-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="99b44-117">-PrivateEndpointName</span></span>
<span data-ttu-id="99b44-118">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="99b44-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b44-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b44-119">-ResourceGroupName</span></span>
<span data-ttu-id="99b44-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99b44-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b44-121">CommonParameters</span></span>
<span data-ttu-id="99b44-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="99b44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b44-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99b44-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b44-124">輸入</span><span class="sxs-lookup"><span data-stu-id="99b44-124">INPUTS</span></span>

### <span data-ttu-id="99b44-125">System.String</span><span class="sxs-lookup"><span data-stu-id="99b44-125">System.String</span></span>

## <span data-ttu-id="99b44-126">輸出</span><span class="sxs-lookup"><span data-stu-id="99b44-126">OUTPUTS</span></span>

### <span data-ttu-id="99b44-127">Microsoft.Azure.Commands.Network.models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="99b44-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="99b44-128">筆記</span><span class="sxs-lookup"><span data-stu-id="99b44-128">NOTES</span></span>

## <span data-ttu-id="99b44-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="99b44-129">RELATED LINKS</span></span>
