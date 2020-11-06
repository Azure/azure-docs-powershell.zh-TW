---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457159"
---
# <span data-ttu-id="3b121-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3b121-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="3b121-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b121-102">SYNOPSIS</span></span>
<span data-ttu-id="3b121-103">取得金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="3b121-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b121-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b121-104">SYNTAX</span></span>

### <span data-ttu-id="3b121-105">ListAllVaultsInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="3b121-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b121-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="3b121-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b121-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="3b121-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b121-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="3b121-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b121-109">說明</span><span class="sxs-lookup"><span data-stu-id="3b121-109">DESCRIPTION</span></span>
<span data-ttu-id="3b121-110">**AzureRmKeyVault** Cmdlet 會取得訂閱中主要電子倉庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b121-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="3b121-111">您可以查看訂閱中的所有主要電子倉庫實例，或依據資源群組或特定的金鑰電子倉庫來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="3b121-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="3b121-112">請注意，雖然在您取得單一金鑰 vault 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="3b121-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="3b121-113">示例</span><span class="sxs-lookup"><span data-stu-id="3b121-113">EXAMPLES</span></span>

### <span data-ttu-id="3b121-114">範例1：取得目前訂閱中的所有主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="3b121-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="3b121-115">這個命令會在您目前的訂閱中取得所有的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="3b121-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="3b121-116">範例2：取得特定的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="3b121-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="3b121-117">這個命令會在您目前的訂閱中取得名為 Contoso03Vault 的主要電子倉庫，然後將它儲存在 $MyVault 變數中。</span><span class="sxs-lookup"><span data-stu-id="3b121-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="3b121-118">您可以檢查 $MyVault 的屬性，以取得關於主要電子倉庫的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3b121-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="3b121-119">範例3：在資源群組中取得金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="3b121-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="3b121-120">這個命令會取得名為 ContosoPayRollResourceGroup 的資源群組中的所有主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="3b121-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="3b121-121">範例4：在您目前的訂閱中取得所有已刪除的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="3b121-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="3b121-122">這個命令會在您目前的訂閱中取得所有已刪除的金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="3b121-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="3b121-123">範例5：取得刪除的主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="3b121-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="3b121-124">這個命令會在您目前的訂閱和 eastus2 區域中取得名為 Contoso03Vault 的已刪除主要電子倉庫資訊。</span><span class="sxs-lookup"><span data-stu-id="3b121-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="3b121-125">參數</span><span class="sxs-lookup"><span data-stu-id="3b121-125">PARAMETERS</span></span>

### <span data-ttu-id="3b121-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b121-126">-DefaultProfile</span></span>
<span data-ttu-id="3b121-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3b121-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b121-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3b121-128">-InRemovedState</span></span>
<span data-ttu-id="3b121-129">指定是否要在輸出中顯示先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="3b121-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="3b121-130">-位置</span><span class="sxs-lookup"><span data-stu-id="3b121-130">-Location</span></span>
<span data-ttu-id="3b121-131">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="3b121-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b121-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b121-132">-ResourceGroupName</span></span>
<span data-ttu-id="3b121-133">指定與要查詢之主要電子倉庫或主要電子倉庫相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b121-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="3b121-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b121-134">-Tag</span></span>
<span data-ttu-id="3b121-135">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="3b121-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3b121-136">例如：</span><span class="sxs-lookup"><span data-stu-id="3b121-136">For example:</span></span>

<span data-ttu-id="3b121-137">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3b121-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3b121-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3b121-138">-VaultName</span></span>
<span data-ttu-id="3b121-139">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b121-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b121-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b121-140">CommonParameters</span></span>
<span data-ttu-id="3b121-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b121-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b121-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b121-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b121-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3b121-143">INPUTS</span></span>

### <span data-ttu-id="3b121-144">所有</span><span class="sxs-lookup"><span data-stu-id="3b121-144">None</span></span>
<span data-ttu-id="3b121-145">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3b121-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b121-146">輸出</span><span class="sxs-lookup"><span data-stu-id="3b121-146">OUTPUTS</span></span>

### <span data-ttu-id="3b121-147">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="3b121-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3b121-148">[System.object]. 清單 ' 1 [KeyVault]。 PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="3b121-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="3b121-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="3b121-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="3b121-150">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="3b121-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="3b121-151">筆記</span><span class="sxs-lookup"><span data-stu-id="3b121-151">NOTES</span></span>

## <span data-ttu-id="3b121-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b121-152">RELATED LINKS</span></span>

[<span data-ttu-id="3b121-153">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3b121-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="3b121-154">移除-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3b121-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
