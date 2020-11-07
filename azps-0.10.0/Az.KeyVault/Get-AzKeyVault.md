---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794684"
---
# <span data-ttu-id="21c13-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="21c13-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="21c13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21c13-102">SYNOPSIS</span></span>
<span data-ttu-id="21c13-103">取得金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="21c13-103">Gets key vaults.</span></span>

## <span data-ttu-id="21c13-104">句法</span><span class="sxs-lookup"><span data-stu-id="21c13-104">SYNTAX</span></span>

### <span data-ttu-id="21c13-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="21c13-105">GetVaultByName</span></span>
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c13-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="21c13-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c13-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21c13-107">ListVaultsByResourceGroup</span></span>
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21c13-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="21c13-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c13-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="21c13-109">ListAllVaultsInSubscription</span></span>
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c13-110">說明</span><span class="sxs-lookup"><span data-stu-id="21c13-110">DESCRIPTION</span></span>
<span data-ttu-id="21c13-111">**AzKeyVault** Cmdlet 會取得訂閱中主要電子倉庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="21c13-111">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="21c13-112">您可以查看訂閱中的所有主要電子倉庫實例，或依據資源群組或特定的金鑰電子倉庫來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="21c13-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="21c13-113">請注意，雖然在您取得單一金鑰 vault 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="21c13-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="21c13-114">示例</span><span class="sxs-lookup"><span data-stu-id="21c13-114">EXAMPLES</span></span>

### <span data-ttu-id="21c13-115">範例1：取得目前訂閱中的所有主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="21c13-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault
```

<span data-ttu-id="21c13-116">這個命令會在您目前的訂閱中取得所有的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="21c13-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="21c13-117">範例2：取得特定的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="21c13-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="21c13-118">這個命令會在您目前的訂閱中取得名為 Contoso03Vault 的主要電子倉庫，然後將它儲存在 $MyVault 變數中。</span><span class="sxs-lookup"><span data-stu-id="21c13-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="21c13-119">您可以檢查 $MyVault 的屬性，以取得關於主要電子倉庫的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="21c13-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="21c13-120">範例3：在資源群組中取得金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="21c13-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="21c13-121">這個命令會取得名為 ContosoPayRollResourceGroup 的資源群組中的所有主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="21c13-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="21c13-122">範例4：在您目前的訂閱中取得所有已刪除的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="21c13-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault -InRemovedState
```

<span data-ttu-id="21c13-123">這個命令會在您目前的訂閱中取得所有已刪除的金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="21c13-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="21c13-124">範例5：取得刪除的主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="21c13-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="21c13-125">這個命令會在您目前的訂閱和 eastus2 區域中取得名為 Contoso03Vault 的已刪除主要電子倉庫資訊。</span><span class="sxs-lookup"><span data-stu-id="21c13-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="21c13-126">參數</span><span class="sxs-lookup"><span data-stu-id="21c13-126">PARAMETERS</span></span>

### <span data-ttu-id="21c13-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c13-127">-DefaultProfile</span></span>
<span data-ttu-id="21c13-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="21c13-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="21c13-129">-InRemovedState</span></span>
<span data-ttu-id="21c13-130">指定是否要在輸出中顯示先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="21c13-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-131">-位置</span><span class="sxs-lookup"><span data-stu-id="21c13-131">-Location</span></span>
<span data-ttu-id="21c13-132">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="21c13-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c13-133">-ResourceGroupName</span></span>
<span data-ttu-id="21c13-134">指定與要查詢之主要電子倉庫或主要電子倉庫相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21c13-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="21c13-135">-Tag</span></span>
<span data-ttu-id="21c13-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="21c13-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="21c13-137">例如：</span><span class="sxs-lookup"><span data-stu-id="21c13-137">For example:</span></span>

<span data-ttu-id="21c13-138">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="21c13-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="21c13-139">-VaultName</span></span>
<span data-ttu-id="21c13-140">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="21c13-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c13-141">CommonParameters</span></span>
<span data-ttu-id="21c13-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21c13-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c13-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21c13-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c13-144">輸入</span><span class="sxs-lookup"><span data-stu-id="21c13-144">INPUTS</span></span>

### <span data-ttu-id="21c13-145">所有</span><span class="sxs-lookup"><span data-stu-id="21c13-145">None</span></span>
<span data-ttu-id="21c13-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="21c13-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21c13-147">輸出</span><span class="sxs-lookup"><span data-stu-id="21c13-147">OUTPUTS</span></span>

### <span data-ttu-id="21c13-148">PSVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="21c13-148">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="21c13-149">[System.object]. 清單 ' 1 [KeyVault]。 PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="21c13-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="21c13-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="21c13-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="21c13-151">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="21c13-151">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="21c13-152">筆記</span><span class="sxs-lookup"><span data-stu-id="21c13-152">NOTES</span></span>

## <span data-ttu-id="21c13-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="21c13-153">RELATED LINKS</span></span>

[<span data-ttu-id="21c13-154">新-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="21c13-154">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="21c13-155">移除-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="21c13-155">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
