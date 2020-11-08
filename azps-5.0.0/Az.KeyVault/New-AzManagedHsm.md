---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141656"
---
# <span data-ttu-id="5074a-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="5074a-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="5074a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5074a-102">SYNOPSIS</span></span>
<span data-ttu-id="5074a-103">建立受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="5074a-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="5074a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5074a-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5074a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5074a-105">DESCRIPTION</span></span>
<span data-ttu-id="5074a-106">**新的-AzManagedHsm** Cmdlet 會在指定的資源群組中建立受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="5074a-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="5074a-107">若要在受管理的 HSM 中新增、移除或列出金鑰，使用者應該透過將使用者識別碼新增至系統管理員來授與許可權。</span><span class="sxs-lookup"><span data-stu-id="5074a-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="5074a-108">示例</span><span class="sxs-lookup"><span data-stu-id="5074a-108">EXAMPLES</span></span>

### <span data-ttu-id="5074a-109">範例1：建立 StandardB1 managed HSM</span><span class="sxs-lookup"><span data-stu-id="5074a-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="5074a-110">這個命令會在位置 eastus2euap 中建立一個名為 myhsm 的受管理 HSM。</span><span class="sxs-lookup"><span data-stu-id="5074a-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="5074a-111">該命令會將受管理的 HSM 新增到名為 myrg1 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="5074a-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="5074a-112">因為命令不會指定 *SKU* 參數的值，所以它會建立 Standard_B1 受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="5074a-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="5074a-113">範例2：建立 CustomB32 managed HSM</span><span class="sxs-lookup"><span data-stu-id="5074a-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="5074a-114">這個命令會建立受管理的 HSM，就像前面的範例所示。</span><span class="sxs-lookup"><span data-stu-id="5074a-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="5074a-115">不過，它會指定 *SKU* 參數的 CustomB32 值，以建立 CustomB32 受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="5074a-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="5074a-116">參數</span><span class="sxs-lookup"><span data-stu-id="5074a-116">PARAMETERS</span></span>

### <span data-ttu-id="5074a-117">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="5074a-117">-Administrator</span></span>
<span data-ttu-id="5074a-118">此受管理的 HSM 池的初始系統管理員物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5074a-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="5074a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5074a-119">-AsJob</span></span>
<span data-ttu-id="5074a-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5074a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5074a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5074a-121">-DefaultProfile</span></span>
<span data-ttu-id="5074a-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5074a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5074a-123">-位置</span><span class="sxs-lookup"><span data-stu-id="5074a-123">-Location</span></span>
<span data-ttu-id="5074a-124">指定要在其中建立金鑰保存庫的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="5074a-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="5074a-125">將命令 Get-AzResourceProvider 與 ProviderNamespace 參數搭配使用，即可查看您的選擇。</span><span class="sxs-lookup"><span data-stu-id="5074a-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="5074a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="5074a-126">-Name</span></span>
<span data-ttu-id="5074a-127">指定要建立的受管理 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5074a-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="5074a-128">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="5074a-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="5074a-129">名稱必須以字母或數位開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="5074a-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="5074a-130">名稱必須是通用唯一的。</span><span class="sxs-lookup"><span data-stu-id="5074a-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="5074a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5074a-131">-ResourceGroupName</span></span>
<span data-ttu-id="5074a-132">指定要在其中建立金鑰保存庫的現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5074a-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="5074a-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="5074a-133">-Sku</span></span>
<span data-ttu-id="5074a-134">指定受管理的 HSM 實例的 SKU。</span><span class="sxs-lookup"><span data-stu-id="5074a-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="5074a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="5074a-135">-Tag</span></span>
<span data-ttu-id="5074a-136">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5074a-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="5074a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="5074a-137">-Confirm</span></span>
<span data-ttu-id="5074a-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5074a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5074a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5074a-139">-WhatIf</span></span>
<span data-ttu-id="5074a-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5074a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5074a-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5074a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5074a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5074a-142">CommonParameters</span></span>
<span data-ttu-id="5074a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5074a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5074a-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5074a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5074a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="5074a-145">INPUTS</span></span>

### <span data-ttu-id="5074a-146">System.object</span><span class="sxs-lookup"><span data-stu-id="5074a-146">System.String</span></span>

### <span data-ttu-id="5074a-147">System.object []</span><span class="sxs-lookup"><span data-stu-id="5074a-147">System.String[]</span></span>

### <span data-ttu-id="5074a-148">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5074a-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5074a-149">輸出</span><span class="sxs-lookup"><span data-stu-id="5074a-149">OUTPUTS</span></span>

### <span data-ttu-id="5074a-150">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="5074a-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="5074a-151">筆記</span><span class="sxs-lookup"><span data-stu-id="5074a-151">NOTES</span></span>

## <span data-ttu-id="5074a-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5074a-152">RELATED LINKS</span></span>

[<span data-ttu-id="5074a-153">AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="5074a-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="5074a-154">移除-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="5074a-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="5074a-155">更新-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="5074a-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)