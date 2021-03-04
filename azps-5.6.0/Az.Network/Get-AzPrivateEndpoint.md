---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 09bd7f919b953c4df09293a75c2c893df4a01b96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902478"
---
# <span data-ttu-id="8e7ff-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e7ff-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="8e7ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7ff-103">取得私人端點</span><span class="sxs-lookup"><span data-stu-id="8e7ff-103">Get a private endpoint</span></span>

## <span data-ttu-id="8e7ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e7ff-104">SYNTAX</span></span>

### <span data-ttu-id="8e7ff-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="8e7ff-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e7ff-106">擴大</span><span class="sxs-lookup"><span data-stu-id="8e7ff-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e7ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="8e7ff-107">DESCRIPTION</span></span>
<span data-ttu-id="8e7ff-108">**Get-AzPrivateEndpoint** Cmdlet 會取得一或多個私人端點。</span><span class="sxs-lookup"><span data-stu-id="8e7ff-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="8e7ff-109">例子</span><span class="sxs-lookup"><span data-stu-id="8e7ff-109">EXAMPLES</span></span>

### <span data-ttu-id="8e7ff-110">範例 1：取回私人端點</span><span class="sxs-lookup"><span data-stu-id="8e7ff-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="8e7ff-111">此命令會獲得資源群組 TestResourceGroup 中名為 MyPrivateEndpoint1 的私人端點</span><span class="sxs-lookup"><span data-stu-id="8e7ff-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="8e7ff-112">範例 2：列出 ResourceGroup 中所有的私人端點</span><span class="sxs-lookup"><span data-stu-id="8e7ff-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="8e7ff-113">此命令會獲得資源群組 TestResourceGroup 中所有的私人結束點</span><span class="sxs-lookup"><span data-stu-id="8e7ff-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="8e7ff-114">參數</span><span class="sxs-lookup"><span data-stu-id="8e7ff-114">PARAMETERS</span></span>

### <span data-ttu-id="8e7ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7ff-115">-DefaultProfile</span></span>
<span data-ttu-id="8e7ff-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e7ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e7ff-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8e7ff-117">-ExpandResource</span></span>
<span data-ttu-id="8e7ff-118">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="8e7ff-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="8e7ff-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e7ff-119">-Name</span></span>
<span data-ttu-id="8e7ff-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7ff-120">The resource name.</span></span>

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

### <span data-ttu-id="8e7ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e7ff-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8e7ff-122">The resource group name.</span></span>

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

### <span data-ttu-id="8e7ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7ff-123">CommonParameters</span></span>
<span data-ttu-id="8e7ff-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e7ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7ff-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e7ff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7ff-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8e7ff-126">INPUTS</span></span>

### <span data-ttu-id="8e7ff-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8e7ff-127">System.String</span></span>

## <span data-ttu-id="8e7ff-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8e7ff-128">OUTPUTS</span></span>

### <span data-ttu-id="8e7ff-129">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8e7ff-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="8e7ff-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8e7ff-130">NOTES</span></span>

## <span data-ttu-id="8e7ff-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e7ff-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e7ff-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e7ff-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="8e7ff-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e7ff-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)