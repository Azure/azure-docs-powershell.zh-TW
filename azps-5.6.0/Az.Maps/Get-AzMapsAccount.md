---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: 420cf84bb946df3d7f2110937aa332e25978aa8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912825"
---
# <span data-ttu-id="2d094-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2d094-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="2d094-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d094-102">SYNOPSIS</span></span>
<span data-ttu-id="2d094-103">獲得帳戶。</span><span class="sxs-lookup"><span data-stu-id="2d094-103">Gets the account.</span></span>

## <span data-ttu-id="2d094-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d094-104">SYNTAX</span></span>

### <span data-ttu-id="2d094-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2d094-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d094-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d094-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d094-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d094-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d094-108">描述</span><span class="sxs-lookup"><span data-stu-id="2d094-108">DESCRIPTION</span></span>
<span data-ttu-id="2d094-109">Cmdlet Get-AzMapsAccount資源群組和名稱，或根據資源識別碼，獲得已配置 Azure 地圖帳戶。此外，它也可以返回 ResourceGroup 中所有帳戶的清單，或目前訂閱的所有 Azure 地圖服務帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="2d094-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="2d094-110">例子</span><span class="sxs-lookup"><span data-stu-id="2d094-110">EXAMPLES</span></span>

### <span data-ttu-id="2d094-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2d094-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="2d094-112">在資源群組 MyResourceGroup 中，獲得名為 MyAccount 的帳戶 （如果有）。</span><span class="sxs-lookup"><span data-stu-id="2d094-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="2d094-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="2d094-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="2d094-114">在資源群組 MyResourceGroup 中，獲得所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="2d094-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="2d094-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="2d094-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="2d094-116">在目前的訂閱中，獲得所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="2d094-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="2d094-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="2d094-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="2d094-118">獲得資源識別碼指定的地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="2d094-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="2d094-119">參數</span><span class="sxs-lookup"><span data-stu-id="2d094-119">PARAMETERS</span></span>

### <span data-ttu-id="2d094-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d094-120">-DefaultProfile</span></span>
<span data-ttu-id="2d094-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d094-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d094-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d094-122">-Name</span></span>
<span data-ttu-id="2d094-123">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2d094-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d094-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d094-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d094-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2d094-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d094-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d094-126">-ResourceId</span></span>
<span data-ttu-id="2d094-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="2d094-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d094-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d094-128">CommonParameters</span></span>
<span data-ttu-id="2d094-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d094-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d094-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2d094-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d094-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2d094-131">INPUTS</span></span>

### <span data-ttu-id="2d094-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2d094-132">System.String</span></span>

## <span data-ttu-id="2d094-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2d094-133">OUTPUTS</span></span>

### <span data-ttu-id="2d094-134">Microsoft.Azure.Commands.Maps.models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2d094-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="2d094-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2d094-135">NOTES</span></span>

## <span data-ttu-id="2d094-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d094-136">RELATED LINKS</span></span>
