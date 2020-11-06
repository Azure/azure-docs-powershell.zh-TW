---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447774"
---
# <span data-ttu-id="b46b2-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b46b2-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="b46b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b46b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b46b2-103">取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="b46b2-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b46b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b46b2-104">SYNTAX</span></span>

### <span data-ttu-id="b46b2-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b46b2-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b46b2-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46b2-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b46b2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b46b2-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b46b2-108">說明</span><span class="sxs-lookup"><span data-stu-id="b46b2-108">DESCRIPTION</span></span>
<span data-ttu-id="b46b2-109">**AzureRmLocationBasedServicesAccount** Cmdlet 會透過資源群組、名稱或資源識別碼，取得已配置的位置的服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="b46b2-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="b46b2-110">此外，它也可以傳回該 ResourceGroup 中所有帳戶的清單，或返回目前訂閱的所有位置的服務帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="b46b2-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="b46b2-111">示例</span><span class="sxs-lookup"><span data-stu-id="b46b2-111">EXAMPLES</span></span>

### <span data-ttu-id="b46b2-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b46b2-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="b46b2-113">取得 [資源群組 MyResourceGroup] 中名為 [我的帳戶] 的帳戶（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b46b2-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="b46b2-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b46b2-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="b46b2-115">在 [資源] 群組 MyResourceGroup 中取得所有位置的服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="b46b2-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b46b2-116">範例3</span><span class="sxs-lookup"><span data-stu-id="b46b2-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="b46b2-117">取得目前訂閱中所有位置的服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="b46b2-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="b46b2-118">範例4</span><span class="sxs-lookup"><span data-stu-id="b46b2-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="b46b2-119">取得由資源識別碼指定的以位置為基礎的服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="b46b2-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="b46b2-120">參數</span><span class="sxs-lookup"><span data-stu-id="b46b2-120">PARAMETERS</span></span>

### <span data-ttu-id="b46b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46b2-121">-DefaultProfile</span></span>
<span data-ttu-id="b46b2-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b46b2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b46b2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b46b2-123">-Name</span></span>
<span data-ttu-id="b46b2-124">[以位置為基礎的服務] 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b46b2-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b46b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b46b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="b46b2-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b46b2-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b46b2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b46b2-127">-ResourceId</span></span>
<span data-ttu-id="b46b2-128">基於位置的服務帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b46b2-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b46b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46b2-129">CommonParameters</span></span>
<span data-ttu-id="b46b2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b46b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46b2-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b46b2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46b2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b46b2-132">INPUTS</span></span>

### <span data-ttu-id="b46b2-133">System.object</span><span class="sxs-lookup"><span data-stu-id="b46b2-133">System.String</span></span>

## <span data-ttu-id="b46b2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b46b2-134">OUTPUTS</span></span>

### <span data-ttu-id="b46b2-135">PSLocationBasedServicesAccount 中的 LocationBasedServices。</span><span class="sxs-lookup"><span data-stu-id="b46b2-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="b46b2-136">這個 Cmdlet 會傳回 **PSLocationBasedServicesAccount** 物件。</span><span class="sxs-lookup"><span data-stu-id="b46b2-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="b46b2-137">您可以修改這個物件，然後使用 [ **設定] AzureRmLocationBasedServices** [套用變更]。</span><span class="sxs-lookup"><span data-stu-id="b46b2-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="b46b2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b46b2-138">NOTES</span></span>

## <span data-ttu-id="b46b2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b46b2-139">RELATED LINKS</span></span>
