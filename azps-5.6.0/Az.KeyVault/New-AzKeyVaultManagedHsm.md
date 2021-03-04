---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 72804d546869f2d003813c8e69c067ad23966fa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914781"
---
# <span data-ttu-id="2904b-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="2904b-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="2904b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2904b-102">SYNOPSIS</span></span>
<span data-ttu-id="2904b-103">建立受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="2904b-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="2904b-104">語法</span><span class="sxs-lookup"><span data-stu-id="2904b-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2904b-105">描述</span><span class="sxs-lookup"><span data-stu-id="2904b-105">DESCRIPTION</span></span>
<span data-ttu-id="2904b-106">**New-AzKeyVaultManagedPvm** Cmdlet 會于指定的資源群組中建立受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="2904b-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="2904b-107">若要新增、移除或列出受管理 HSM 中的金鑰，使用者應新增使用者識別碼至系統管理員以授予許可權。</span><span class="sxs-lookup"><span data-stu-id="2904b-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="2904b-108">例子</span><span class="sxs-lookup"><span data-stu-id="2904b-108">EXAMPLES</span></span>

### <span data-ttu-id="2904b-109">範例 1：建立 StandardB1 Managed HSM</span><span class="sxs-lookup"><span data-stu-id="2904b-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="2904b-110">此命令會建立一個名為 mym 的受管理 HSM，位於 eastus2到ap 位置。</span><span class="sxs-lookup"><span data-stu-id="2904b-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="2904b-111">該命令會將受管理的 HSM 新增到名為 myrg1 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2904b-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="2904b-112">由於命令不會為 *SKU* 參數指定值，因此會建立受Standard_B1 HSM。</span><span class="sxs-lookup"><span data-stu-id="2904b-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="2904b-113">範例 2：建立 CustomB32 managed HSM</span><span class="sxs-lookup"><span data-stu-id="2904b-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="2904b-114">此命令會建立受管理的 HSM，就像上一個範例一樣。</span><span class="sxs-lookup"><span data-stu-id="2904b-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="2904b-115">不過，它會指定 *SKU* 參數的 CustomB32 值，以建立 CustomB32 Managed HSM。</span><span class="sxs-lookup"><span data-stu-id="2904b-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="2904b-116">參數</span><span class="sxs-lookup"><span data-stu-id="2904b-116">PARAMETERS</span></span>

### <span data-ttu-id="2904b-117">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="2904b-117">-Administrator</span></span>
<span data-ttu-id="2904b-118">此受管理的 HSM 資料庫的初始系統管理員物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="2904b-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2904b-119">-AsJob</span></span>
<span data-ttu-id="2904b-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2904b-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2904b-121">-DefaultProfile</span></span>
<span data-ttu-id="2904b-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2904b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2904b-123">-位置</span><span class="sxs-lookup"><span data-stu-id="2904b-123">-Location</span></span>
<span data-ttu-id="2904b-124">指定要建立金鑰庫的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="2904b-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="2904b-125">使用Get-AzResourceProvider ProviderNamespace 參數來查看您的選擇。</span><span class="sxs-lookup"><span data-stu-id="2904b-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="2904b-126">-Name</span></span>
<span data-ttu-id="2904b-127">指定要建立之受管理 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2904b-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="2904b-128">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="2904b-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="2904b-129">名稱必須以字母或數位做為開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="2904b-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="2904b-130">名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2904b-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2904b-131">-ResourceGroupName</span></span>
<span data-ttu-id="2904b-132">指定要建立金鑰庫之現有資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2904b-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="2904b-133">-Sku</span></span>
<span data-ttu-id="2904b-134">指定受管理 HSM 實例的 SKU。</span><span class="sxs-lookup"><span data-stu-id="2904b-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-135">-標記</span><span class="sxs-lookup"><span data-stu-id="2904b-135">-Tag</span></span>
<span data-ttu-id="2904b-136">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2904b-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="2904b-137">-Confirm</span></span>
<span data-ttu-id="2904b-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2904b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2904b-139">-WhatIf</span></span>
<span data-ttu-id="2904b-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2904b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2904b-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2904b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2904b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2904b-142">CommonParameters</span></span>
<span data-ttu-id="2904b-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2904b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2904b-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2904b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2904b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="2904b-145">INPUTS</span></span>

### <span data-ttu-id="2904b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2904b-146">System.String</span></span>

### <span data-ttu-id="2904b-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2904b-147">System.String[]</span></span>

### <span data-ttu-id="2904b-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2904b-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2904b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="2904b-149">OUTPUTS</span></span>

### <span data-ttu-id="2904b-150">Microsoft.Azure.Commands.KeyVault.models.PSManagedPvm</span><span class="sxs-lookup"><span data-stu-id="2904b-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="2904b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="2904b-151">NOTES</span></span>

## <span data-ttu-id="2904b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="2904b-152">RELATED LINKS</span></span>

[<span data-ttu-id="2904b-153">Get-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="2904b-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="2904b-154">Remove-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="2904b-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="2904b-155">Update-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="2904b-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)