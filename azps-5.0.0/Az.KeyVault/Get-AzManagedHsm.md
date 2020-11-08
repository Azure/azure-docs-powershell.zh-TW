---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139173"
---
# <span data-ttu-id="e5c06-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e5c06-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="e5c06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5c06-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c06-103">取得受管理的 Hsm。</span><span class="sxs-lookup"><span data-stu-id="e5c06-103">Get managed HSMs.</span></span>

## <span data-ttu-id="e5c06-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5c06-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c06-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5c06-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c06-106">**AzManagedHsm** Cmdlet 會取得訂閱中受管理的 hsm 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5c06-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="e5c06-107">您可以在訂閱中查看所有受管理的 Hsm 實例，或依據資源群組或特定受管理的 HSM 來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="e5c06-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="e5c06-108">請注意，雖然在您取得單一受管理的 HSM 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="e5c06-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="e5c06-109">示例</span><span class="sxs-lookup"><span data-stu-id="e5c06-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c06-110">範例1：在您目前的訂閱中取得所有受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="e5c06-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e5c06-111">這個命令會在您目前的訂閱中取得所有受管理的 Hsm。</span><span class="sxs-lookup"><span data-stu-id="e5c06-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="e5c06-112">範例2：取得特定的受管理 HSM</span><span class="sxs-lookup"><span data-stu-id="e5c06-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e5c06-113">這個命令會在您目前的訂閱中取得名為 myhsm 的受管理 HSM。</span><span class="sxs-lookup"><span data-stu-id="e5c06-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="e5c06-114">範例3：在資源群組中取得受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="e5c06-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e5c06-115">這個命令會取得名為 myrg1 的資源群組中的所有受管理的 Hsm。</span><span class="sxs-lookup"><span data-stu-id="e5c06-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="e5c06-116">範例4：使用篩選來取得受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="e5c06-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e5c06-117">這個命令會取得訂閱中以 "myhsm" 為開頭的所有 managed Hsm。</span><span class="sxs-lookup"><span data-stu-id="e5c06-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="e5c06-118">參數</span><span class="sxs-lookup"><span data-stu-id="e5c06-118">PARAMETERS</span></span>

### <span data-ttu-id="e5c06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c06-119">-DefaultProfile</span></span>
<span data-ttu-id="e5c06-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5c06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c06-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5c06-121">-Name</span></span>
<span data-ttu-id="e5c06-122">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c06-122">HSM name.</span></span> <span data-ttu-id="e5c06-123">Cmdlet 根據名稱和目前所選的環境來構造 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e5c06-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c06-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c06-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5c06-125">指定與被查詢之受管理的 HSM 相關聯的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c06-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c06-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5c06-126">-Tag</span></span>
<span data-ttu-id="e5c06-127">指定指定標記的索引鍵和選用值，以篩選受管理的 Hsm 清單。</span><span class="sxs-lookup"><span data-stu-id="e5c06-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="e5c06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c06-128">CommonParameters</span></span>
<span data-ttu-id="e5c06-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5c06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c06-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5c06-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c06-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e5c06-131">INPUTS</span></span>

### <span data-ttu-id="e5c06-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e5c06-132">System.String</span></span>

### <span data-ttu-id="e5c06-133">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5c06-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5c06-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e5c06-134">OUTPUTS</span></span>

### <span data-ttu-id="e5c06-135">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e5c06-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="e5c06-136">PSKeyVaultIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e5c06-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="e5c06-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e5c06-137">NOTES</span></span>

## <span data-ttu-id="e5c06-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5c06-138">RELATED LINKS</span></span>

[<span data-ttu-id="e5c06-139">新-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e5c06-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="e5c06-140">移除-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e5c06-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="e5c06-141">更新-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e5c06-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)