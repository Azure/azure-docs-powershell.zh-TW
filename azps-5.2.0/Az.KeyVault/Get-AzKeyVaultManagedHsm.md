---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276240"
---
# <span data-ttu-id="8c247-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8c247-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="8c247-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c247-102">SYNOPSIS</span></span>
<span data-ttu-id="8c247-103">取得受管理的 Hsm。</span><span class="sxs-lookup"><span data-stu-id="8c247-103">Get managed HSMs.</span></span>

## <span data-ttu-id="8c247-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c247-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c247-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c247-105">DESCRIPTION</span></span>
<span data-ttu-id="8c247-106">**AzKeyVaultManagedHsm** Cmdlet 會取得訂閱中受管理的 hsm 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c247-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="8c247-107">您可以在訂閱中查看所有受管理的 Hsm 實例，或依據資源群組或特定受管理的 HSM 來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="8c247-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="8c247-108">請注意，雖然在您取得單一受管理的 HSM 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="8c247-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="8c247-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c247-109">EXAMPLES</span></span>

### <span data-ttu-id="8c247-110">範例1：在您目前的訂閱中取得所有受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="8c247-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="8c247-111">這個命令會在您目前的訂閱中取得所有受管理的 Hsm。</span><span class="sxs-lookup"><span data-stu-id="8c247-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="8c247-112">範例2：取得特定的受管理 HSM</span><span class="sxs-lookup"><span data-stu-id="8c247-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="8c247-113">這個命令會在您目前的訂閱中取得名為 myhsm 的受管理 HSM。</span><span class="sxs-lookup"><span data-stu-id="8c247-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="8c247-114">範例3：在資源群組中取得受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="8c247-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="8c247-115">這個命令會取得名為 myrg1 的資源群組中的所有受管理的 Hsm。</span><span class="sxs-lookup"><span data-stu-id="8c247-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="8c247-116">範例4：使用篩選來取得受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="8c247-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="8c247-117">這個命令會取得訂閱中以 "myhsm" 為開頭的所有 managed Hsm。</span><span class="sxs-lookup"><span data-stu-id="8c247-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="8c247-118">參數</span><span class="sxs-lookup"><span data-stu-id="8c247-118">PARAMETERS</span></span>

### <span data-ttu-id="8c247-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c247-119">-DefaultProfile</span></span>
<span data-ttu-id="8c247-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c247-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c247-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c247-121">-Name</span></span>
<span data-ttu-id="8c247-122">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="8c247-122">HSM name.</span></span> <span data-ttu-id="8c247-123">Cmdlet 根據名稱和目前所選的環境來構造 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="8c247-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8c247-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c247-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c247-125">指定與被查詢之受管理的 HSM 相關聯的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c247-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

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

### <span data-ttu-id="8c247-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c247-126">-Tag</span></span>
<span data-ttu-id="8c247-127">指定指定標記的索引鍵和選用值，以篩選受管理的 Hsm 清單。</span><span class="sxs-lookup"><span data-stu-id="8c247-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="8c247-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c247-128">CommonParameters</span></span>
<span data-ttu-id="8c247-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c247-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c247-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c247-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c247-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8c247-131">INPUTS</span></span>

### <span data-ttu-id="8c247-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8c247-132">System.String</span></span>

### <span data-ttu-id="8c247-133">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8c247-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8c247-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8c247-134">OUTPUTS</span></span>

### <span data-ttu-id="8c247-135">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8c247-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="8c247-136">PSKeyVaultIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8c247-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="8c247-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8c247-137">NOTES</span></span>

## <span data-ttu-id="8c247-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c247-138">RELATED LINKS</span></span>

[<span data-ttu-id="8c247-139">新-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8c247-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="8c247-140">移除-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8c247-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="8c247-141">更新-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="8c247-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)