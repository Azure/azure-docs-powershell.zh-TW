---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: 7ea94e2e7e4c3e54d67beef367dffee001e94652
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611864"
---
# <span data-ttu-id="1b5e4-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1b5e4-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="1b5e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5e4-103">取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-103">Gets the account.</span></span>

## <span data-ttu-id="1b5e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b5e4-104">SYNTAX</span></span>

### <span data-ttu-id="1b5e4-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1b5e4-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b5e4-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b5e4-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b5e4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b5e4-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b5e4-108">說明</span><span class="sxs-lookup"><span data-stu-id="1b5e4-108">DESCRIPTION</span></span>
<span data-ttu-id="1b5e4-109">Get-AzMapsAccount Cmdlet 會取得已預配的 Azure 地圖帳戶（依資源群組和名稱，或由資源識別碼）。此外，它還可以傳回 ResourceGroup 中所有帳戶的清單，或針對目前訂閱的所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="1b5e4-110">示例</span><span class="sxs-lookup"><span data-stu-id="1b5e4-110">EXAMPLES</span></span>

### <span data-ttu-id="1b5e4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1b5e4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="1b5e4-112">取得 [資源群組 MyResourceGroup] 中名為 [我的帳戶] 的帳戶（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="1b5e4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1b5e4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="1b5e4-114">取得 [資源群組 MyResourceGroup] 中的所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1b5e4-115">範例3</span><span class="sxs-lookup"><span data-stu-id="1b5e4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="1b5e4-116">取得目前訂閱中的所有 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="1b5e4-117">範例4</span><span class="sxs-lookup"><span data-stu-id="1b5e4-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="1b5e4-118">取得資源識別碼所指定的地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="1b5e4-119">參數</span><span class="sxs-lookup"><span data-stu-id="1b5e4-119">PARAMETERS</span></span>

### <span data-ttu-id="1b5e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5e4-120">-DefaultProfile</span></span>
<span data-ttu-id="1b5e4-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b5e4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b5e4-122">-Name</span></span>
<span data-ttu-id="1b5e4-123">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="1b5e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b5e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b5e4-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1b5e4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b5e4-126">-ResourceId</span></span>
<span data-ttu-id="1b5e4-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="1b5e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5e4-128">CommonParameters</span></span>
<span data-ttu-id="1b5e4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5e4-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b5e4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5e4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1b5e4-131">INPUTS</span></span>

### <span data-ttu-id="1b5e4-132">System.object</span><span class="sxs-lookup"><span data-stu-id="1b5e4-132">System.String</span></span>

## <span data-ttu-id="1b5e4-133">輸出</span><span class="sxs-lookup"><span data-stu-id="1b5e4-133">OUTPUTS</span></span>

### <span data-ttu-id="1b5e4-134">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b5e4-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="1b5e4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1b5e4-135">NOTES</span></span>

## <span data-ttu-id="1b5e4-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b5e4-136">RELATED LINKS</span></span>
