---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 7cbcf722b71919096ca2c7d1dc3201ad2fe42f2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801657"
---
# <span data-ttu-id="b0384-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b0384-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="b0384-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0384-102">SYNOPSIS</span></span>
<span data-ttu-id="b0384-103">取得金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b0384-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0384-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0384-104">SYNTAX</span></span>

### <span data-ttu-id="b0384-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="b0384-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0384-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b0384-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0384-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b0384-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0384-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="b0384-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0384-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="b0384-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0384-110">說明</span><span class="sxs-lookup"><span data-stu-id="b0384-110">DESCRIPTION</span></span>
<span data-ttu-id="b0384-111">**AzureRmKeyVault** Cmdlet 會取得訂閱中主要電子倉庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b0384-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="b0384-112">您可以查看訂閱中的所有主要電子倉庫實例，或依據資源群組或特定的金鑰電子倉庫來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="b0384-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="b0384-113">請注意，雖然在您取得單一金鑰 vault 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="b0384-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="b0384-114">示例</span><span class="sxs-lookup"><span data-stu-id="b0384-114">EXAMPLES</span></span>

### <span data-ttu-id="b0384-115">範例1：取得目前訂閱中的所有主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="b0384-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="b0384-116">這個命令會在您目前的訂閱中取得所有的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b0384-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="b0384-117">範例2：取得特定的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="b0384-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="b0384-118">這個命令會在您目前的訂閱中取得名為 Contoso03Vault 的主要電子倉庫，然後將它儲存在 $MyVault 變數中。</span><span class="sxs-lookup"><span data-stu-id="b0384-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="b0384-119">您可以檢查 $MyVault 的屬性，以取得關於主要電子倉庫的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b0384-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="b0384-120">範例3：在資源群組中取得金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="b0384-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="b0384-121">這個命令會取得名為 ContosoPayRollResourceGroup 的資源群組中的所有主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b0384-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="b0384-122">範例4：在您目前的訂閱中取得所有已刪除的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="b0384-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="b0384-123">這個命令會在您目前的訂閱中取得所有已刪除的金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b0384-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="b0384-124">範例5：取得刪除的主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="b0384-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="b0384-125">這個命令會在您目前的訂閱和 eastus2 區域中取得名為 Contoso03Vault 的已刪除主要電子倉庫資訊。</span><span class="sxs-lookup"><span data-stu-id="b0384-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="b0384-126">參數</span><span class="sxs-lookup"><span data-stu-id="b0384-126">PARAMETERS</span></span>

### <span data-ttu-id="b0384-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0384-127">-DefaultProfile</span></span>
<span data-ttu-id="b0384-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b0384-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0384-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b0384-129">-InRemovedState</span></span>
<span data-ttu-id="b0384-130">指定是否要在輸出中顯示先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b0384-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="b0384-131">-位置</span><span class="sxs-lookup"><span data-stu-id="b0384-131">-Location</span></span>
<span data-ttu-id="b0384-132">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="b0384-132">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="b0384-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0384-133">-ResourceGroupName</span></span>
<span data-ttu-id="b0384-134">指定與要查詢之主要電子倉庫或主要電子倉庫相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0384-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="b0384-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b0384-135">-Tag</span></span>
<span data-ttu-id="b0384-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="b0384-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b0384-137">例如：</span><span class="sxs-lookup"><span data-stu-id="b0384-137">For example:</span></span>

<span data-ttu-id="b0384-138">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b0384-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b0384-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b0384-139">-VaultName</span></span>
<span data-ttu-id="b0384-140">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0384-140">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="b0384-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0384-141">CommonParameters</span></span>
<span data-ttu-id="b0384-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0384-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0384-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0384-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0384-144">輸入</span><span class="sxs-lookup"><span data-stu-id="b0384-144">INPUTS</span></span>

## <span data-ttu-id="b0384-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b0384-145">OUTPUTS</span></span>

### <span data-ttu-id="b0384-146">PSVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="b0384-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="b0384-147">[System.object]. 清單 ' 1 [KeyVault]。 PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="b0384-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="b0384-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b0384-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="b0384-149">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="b0384-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="b0384-150">筆記</span><span class="sxs-lookup"><span data-stu-id="b0384-150">NOTES</span></span>

## <span data-ttu-id="b0384-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0384-151">RELATED LINKS</span></span>

[<span data-ttu-id="b0384-152">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b0384-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="b0384-153">移除-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b0384-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
