---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127002"
---
# <span data-ttu-id="5d4f3-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5d4f3-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5d4f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4f3-103">取得 [私人 DNS 區域] 群組</span><span class="sxs-lookup"><span data-stu-id="5d4f3-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="5d4f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d4f3-104">SYNTAX</span></span>

### <span data-ttu-id="5d4f3-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5d4f3-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4f3-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="5d4f3-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d4f3-107">說明</span><span class="sxs-lookup"><span data-stu-id="5d4f3-107">DESCRIPTION</span></span>
<span data-ttu-id="5d4f3-108">**AzPrivateDnsZoneGroup** Cmdlet 會取得一或多個私人 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="5d4f3-109">示例</span><span class="sxs-lookup"><span data-stu-id="5d4f3-109">EXAMPLES</span></span>

### <span data-ttu-id="5d4f3-110">範例1：檢索私人 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="5d4f3-110">Example 1: Retrieve private DNS zone group</span></span>
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

<span data-ttu-id="5d4f3-111">上述範例會在資源群組 rg 中取得名為 dnsgroup1 的專用 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="5d4f3-112">參數</span><span class="sxs-lookup"><span data-stu-id="5d4f3-112">PARAMETERS</span></span>

### <span data-ttu-id="5d4f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4f3-113">-DefaultProfile</span></span>
<span data-ttu-id="5d4f3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d4f3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d4f3-115">-Name</span></span>
<span data-ttu-id="5d4f3-116">專用 dns 區域群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="5d4f3-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="5d4f3-117">-PrivateEndpointName</span></span>
<span data-ttu-id="5d4f3-118">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="5d4f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d4f3-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d4f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4f3-121">CommonParameters</span></span>
<span data-ttu-id="5d4f3-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4f3-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5d4f3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4f3-124">輸入</span><span class="sxs-lookup"><span data-stu-id="5d4f3-124">INPUTS</span></span>

### <span data-ttu-id="5d4f3-125">System.object</span><span class="sxs-lookup"><span data-stu-id="5d4f3-125">System.String</span></span>

## <span data-ttu-id="5d4f3-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5d4f3-126">OUTPUTS</span></span>

### <span data-ttu-id="5d4f3-127">PSPrivateDnsZoneGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5d4f3-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5d4f3-128">筆記</span><span class="sxs-lookup"><span data-stu-id="5d4f3-128">NOTES</span></span>

## <span data-ttu-id="5d4f3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d4f3-129">RELATED LINKS</span></span>
