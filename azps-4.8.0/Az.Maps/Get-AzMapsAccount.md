---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970466"
---
# <span data-ttu-id="d2d6a-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="d2d6a-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="d2d6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d6a-103">取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-103">Gets the account.</span></span>

## <span data-ttu-id="d2d6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2d6a-104">SYNTAX</span></span>

### <span data-ttu-id="d2d6a-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d2d6a-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2d6a-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2d6a-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2d6a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2d6a-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2d6a-108">說明</span><span class="sxs-lookup"><span data-stu-id="d2d6a-108">DESCRIPTION</span></span>
<span data-ttu-id="d2d6a-109">Get-AzMapsAccount Cmdlet 會取得已預配的 Azure 地圖帳戶（依資源群組和名稱，或由資源識別碼）。此外，它還可以傳回 ResourceGroup 中所有帳戶的清單，或針對目前訂閱的所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="d2d6a-110">示例</span><span class="sxs-lookup"><span data-stu-id="d2d6a-110">EXAMPLES</span></span>

### <span data-ttu-id="d2d6a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d2d6a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="d2d6a-112">取得 [資源群組 MyResourceGroup] 中名為 [我的帳戶] 的帳戶（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="d2d6a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d2d6a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="d2d6a-114">取得 [資源群組 MyResourceGroup] 中的所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="d2d6a-115">範例3</span><span class="sxs-lookup"><span data-stu-id="d2d6a-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="d2d6a-116">取得目前訂閱中的所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="d2d6a-117">範例4</span><span class="sxs-lookup"><span data-stu-id="d2d6a-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="d2d6a-118">取得資源識別碼所指定的地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="d2d6a-119">參數</span><span class="sxs-lookup"><span data-stu-id="d2d6a-119">PARAMETERS</span></span>

### <span data-ttu-id="d2d6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d6a-120">-DefaultProfile</span></span>
<span data-ttu-id="d2d6a-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2d6a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2d6a-122">-Name</span></span>
<span data-ttu-id="d2d6a-123">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="d2d6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2d6a-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2d6a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2d6a-126">-ResourceId</span></span>
<span data-ttu-id="d2d6a-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="d2d6a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d6a-128">CommonParameters</span></span>
<span data-ttu-id="d2d6a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d6a-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2d6a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d6a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d2d6a-131">INPUTS</span></span>

### <span data-ttu-id="d2d6a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="d2d6a-132">System.String</span></span>

## <span data-ttu-id="d2d6a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d2d6a-133">OUTPUTS</span></span>

### <span data-ttu-id="d2d6a-134">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d2d6a-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="d2d6a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d2d6a-135">NOTES</span></span>

## <span data-ttu-id="d2d6a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2d6a-136">RELATED LINKS</span></span>
