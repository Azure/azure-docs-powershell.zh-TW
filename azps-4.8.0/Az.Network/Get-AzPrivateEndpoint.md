---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126499"
---
# <span data-ttu-id="05c34-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05c34-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="05c34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05c34-102">SYNOPSIS</span></span>
<span data-ttu-id="05c34-103">取得私人端點</span><span class="sxs-lookup"><span data-stu-id="05c34-103">Get a private endpoint</span></span>

## <span data-ttu-id="05c34-104">句法</span><span class="sxs-lookup"><span data-stu-id="05c34-104">SYNTAX</span></span>

### <span data-ttu-id="05c34-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="05c34-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05c34-106">擴充</span><span class="sxs-lookup"><span data-stu-id="05c34-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05c34-107">說明</span><span class="sxs-lookup"><span data-stu-id="05c34-107">DESCRIPTION</span></span>
<span data-ttu-id="05c34-108">**AzPrivateEndpoint** Cmdlet 會取得一或多個私人端點。</span><span class="sxs-lookup"><span data-stu-id="05c34-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="05c34-109">示例</span><span class="sxs-lookup"><span data-stu-id="05c34-109">EXAMPLES</span></span>

### <span data-ttu-id="05c34-110">範例1：檢索私人端點</span><span class="sxs-lookup"><span data-stu-id="05c34-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="05c34-111">這個命令會在 [資源] 群組 TestResourceGroup 中取得名為 MyPrivateEndpoint1 的專用端點。</span><span class="sxs-lookup"><span data-stu-id="05c34-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="05c34-112">範例2：列出 ResourceGroup 中的所有私人端點</span><span class="sxs-lookup"><span data-stu-id="05c34-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="05c34-113">這個命令會取得 [資源群組] TestResourceGroup 中的所有私人端點</span><span class="sxs-lookup"><span data-stu-id="05c34-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="05c34-114">參數</span><span class="sxs-lookup"><span data-stu-id="05c34-114">PARAMETERS</span></span>

### <span data-ttu-id="05c34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c34-115">-DefaultProfile</span></span>
<span data-ttu-id="05c34-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05c34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05c34-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="05c34-117">-ExpandResource</span></span>
<span data-ttu-id="05c34-118">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="05c34-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c34-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="05c34-119">-Name</span></span>
<span data-ttu-id="05c34-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="05c34-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c34-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c34-121">-ResourceGroupName</span></span>
<span data-ttu-id="05c34-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05c34-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c34-123">CommonParameters</span></span>
<span data-ttu-id="05c34-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05c34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c34-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="05c34-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c34-126">輸入</span><span class="sxs-lookup"><span data-stu-id="05c34-126">INPUTS</span></span>

### <span data-ttu-id="05c34-127">System.object</span><span class="sxs-lookup"><span data-stu-id="05c34-127">System.String</span></span>

## <span data-ttu-id="05c34-128">輸出</span><span class="sxs-lookup"><span data-stu-id="05c34-128">OUTPUTS</span></span>

### <span data-ttu-id="05c34-129">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="05c34-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="05c34-130">筆記</span><span class="sxs-lookup"><span data-stu-id="05c34-130">NOTES</span></span>

## <span data-ttu-id="05c34-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="05c34-131">RELATED LINKS</span></span>

[<span data-ttu-id="05c34-132">新-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05c34-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="05c34-133">移除-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05c34-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)