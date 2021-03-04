---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: b65fed5670f34072504c736283ba12e51086d3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913189"
---
# <span data-ttu-id="a2747-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a2747-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="a2747-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2747-102">SYNOPSIS</span></span>
<span data-ttu-id="a2747-103">取得受管理的 HSMS。</span><span class="sxs-lookup"><span data-stu-id="a2747-103">Get managed HSMs.</span></span>

## <span data-ttu-id="a2747-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2747-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2747-105">描述</span><span class="sxs-lookup"><span data-stu-id="a2747-105">DESCRIPTION</span></span>
<span data-ttu-id="a2747-106">**Get-AzKeyVaultManagedPvm** Cmdlet 會取得訂閱中受管理的 HSMS 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a2747-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="a2747-107">您可以查看訂閱中所有受管理的 HSMS 實例，或根據資源群組或特定受管理的 HSM 篩選結果。</span><span class="sxs-lookup"><span data-stu-id="a2747-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="a2747-108">請注意，雖然當您取得單一受管理的 HSM 時，此 Cmdlet 可選擇性指定資源群組，但您應這麼做以提升績效。</span><span class="sxs-lookup"><span data-stu-id="a2747-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="a2747-109">例子</span><span class="sxs-lookup"><span data-stu-id="a2747-109">EXAMPLES</span></span>

### <span data-ttu-id="a2747-110">範例 1：取得目前訂閱中所有受管理的 HSMS</span><span class="sxs-lookup"><span data-stu-id="a2747-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="a2747-111">此命令會獲得您目前訂閱中所有受管理的 HSMS。</span><span class="sxs-lookup"><span data-stu-id="a2747-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="a2747-112">範例 2：取得特定的受管理 HSM</span><span class="sxs-lookup"><span data-stu-id="a2747-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="a2747-113">此命令會獲得您目前訂閱中名為 mym 的受管理 HSM。</span><span class="sxs-lookup"><span data-stu-id="a2747-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="a2747-114">範例 3：在資源群組中取得受管理的 HSMS</span><span class="sxs-lookup"><span data-stu-id="a2747-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="a2747-115">此命令會獲得資源群組中名為 myrg1 的所有受管理的 HSMS。</span><span class="sxs-lookup"><span data-stu-id="a2747-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="a2747-116">範例 4：使用篩選取得受管理的 HSMS</span><span class="sxs-lookup"><span data-stu-id="a2747-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="a2747-117">此命令會獲得訂閱中以 "mydm" 做為開始的所有受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a2747-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="a2747-118">參數</span><span class="sxs-lookup"><span data-stu-id="a2747-118">PARAMETERS</span></span>

### <span data-ttu-id="a2747-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2747-119">-DefaultProfile</span></span>
<span data-ttu-id="a2747-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2747-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2747-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2747-121">-Name</span></span>
<span data-ttu-id="a2747-122">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="a2747-122">HSM name.</span></span> <span data-ttu-id="a2747-123">Cmdlet 會根據名稱和目前選取的環境來建構 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a2747-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a2747-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2747-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2747-125">指定與所查詢受管理的 HSM 相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a2747-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a2747-126">-標記</span><span class="sxs-lookup"><span data-stu-id="a2747-126">-Tag</span></span>
<span data-ttu-id="a2747-127">指定指定標記的金鑰和選擇性值，以篩選受管理的 HSMS 清單。</span><span class="sxs-lookup"><span data-stu-id="a2747-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2747-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2747-128">CommonParameters</span></span>
<span data-ttu-id="a2747-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2747-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2747-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2747-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2747-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a2747-131">INPUTS</span></span>

### <span data-ttu-id="a2747-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a2747-132">System.String</span></span>

### <span data-ttu-id="a2747-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2747-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2747-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a2747-134">OUTPUTS</span></span>

### <span data-ttu-id="a2747-135">Microsoft.Azure.Commands.KeyVault.models.PSManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2747-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="a2747-136">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a2747-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="a2747-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a2747-137">NOTES</span></span>

## <span data-ttu-id="a2747-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2747-138">RELATED LINKS</span></span>

[<span data-ttu-id="a2747-139">New-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2747-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="a2747-140">Remove-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2747-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="a2747-141">Update-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2747-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)