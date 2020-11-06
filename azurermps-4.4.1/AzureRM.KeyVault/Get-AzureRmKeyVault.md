---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446797"
---
# <span data-ttu-id="d5de9-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d5de9-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="d5de9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5de9-102">SYNOPSIS</span></span>
<span data-ttu-id="d5de9-103">取得金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="d5de9-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5de9-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5de9-104">SYNTAX</span></span>

### <span data-ttu-id="d5de9-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="d5de9-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5de9-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="d5de9-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5de9-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d5de9-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5de9-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="d5de9-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5de9-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="d5de9-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5de9-110">說明</span><span class="sxs-lookup"><span data-stu-id="d5de9-110">DESCRIPTION</span></span>
<span data-ttu-id="d5de9-111">**AzureRmKeyVault** Cmdlet 會取得訂閱中主要電子倉庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5de9-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="d5de9-112">您可以查看訂閱中的所有主要電子倉庫實例，或依據資源群組或特定的金鑰電子倉庫來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="d5de9-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="d5de9-113">請注意，雖然在您取得單一金鑰 vault 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="d5de9-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="d5de9-114">示例</span><span class="sxs-lookup"><span data-stu-id="d5de9-114">EXAMPLES</span></span>

### <span data-ttu-id="d5de9-115">範例1：取得目前訂閱中的所有主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="d5de9-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="d5de9-116">這個命令會在您目前的訂閱中取得所有的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="d5de9-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="d5de9-117">範例2：取得特定的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="d5de9-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="d5de9-118">這個命令會在您目前的訂閱中取得名為 Contoso03Vault 的主要電子倉庫，然後將它儲存在 $MyVault 變數中。</span><span class="sxs-lookup"><span data-stu-id="d5de9-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="d5de9-119">您可以檢查 $MyVault 的屬性，以取得關於主要電子倉庫的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d5de9-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="d5de9-120">範例3：在資源群組中取得金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="d5de9-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="d5de9-121">這個命令會取得名為 ContosoPayRollResourceGroup 的資源群組中的所有主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="d5de9-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="d5de9-122">範例4：在您目前的訂閱中取得所有已刪除的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="d5de9-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="d5de9-123">這個命令會在您目前的訂閱中取得所有已刪除的金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="d5de9-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="d5de9-124">範例5：取得刪除的主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="d5de9-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="d5de9-125">這個命令會在您目前的訂閱和 eastus2 區域中取得名為 Contoso03Vault 的已刪除主要電子倉庫資訊。</span><span class="sxs-lookup"><span data-stu-id="d5de9-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="d5de9-126">參數</span><span class="sxs-lookup"><span data-stu-id="d5de9-126">PARAMETERS</span></span>

### <span data-ttu-id="d5de9-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d5de9-127">-InRemovedState</span></span>
<span data-ttu-id="d5de9-128">指定是否要在輸出中顯示先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="d5de9-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5de9-129">-位置</span><span class="sxs-lookup"><span data-stu-id="d5de9-129">-Location</span></span>
<span data-ttu-id="d5de9-130">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="d5de9-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5de9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5de9-131">-ResourceGroupName</span></span>
<span data-ttu-id="d5de9-132">指定與要查詢之主要電子倉庫或主要電子倉庫相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5de9-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5de9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5de9-133">-Tag</span></span>
<span data-ttu-id="d5de9-134">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d5de9-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d5de9-135">例如：</span><span class="sxs-lookup"><span data-stu-id="d5de9-135">For example:</span></span>

<span data-ttu-id="d5de9-136">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d5de9-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5de9-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d5de9-137">-VaultName</span></span>
<span data-ttu-id="d5de9-138">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5de9-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5de9-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5de9-139">-DefaultProfile</span></span>
<span data-ttu-id="d5de9-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5de9-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5de9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5de9-141">CommonParameters</span></span>
<span data-ttu-id="d5de9-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5de9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5de9-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5de9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5de9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="d5de9-144">INPUTS</span></span>

## <span data-ttu-id="d5de9-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d5de9-145">OUTPUTS</span></span>

### <span data-ttu-id="d5de9-146">PSVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d5de9-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="d5de9-147">[System.object]. 清單 ' 1 [KeyVault]。 PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="d5de9-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="d5de9-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="d5de9-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="d5de9-149">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="d5de9-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="d5de9-150">筆記</span><span class="sxs-lookup"><span data-stu-id="d5de9-150">NOTES</span></span>

## <span data-ttu-id="d5de9-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5de9-151">RELATED LINKS</span></span>

[<span data-ttu-id="d5de9-152">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d5de9-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="d5de9-153">移除-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d5de9-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
