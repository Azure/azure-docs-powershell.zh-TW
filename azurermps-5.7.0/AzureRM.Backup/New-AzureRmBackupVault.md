---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453160"
---
# <span data-ttu-id="78856-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="78856-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="78856-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78856-102">SYNOPSIS</span></span>
<span data-ttu-id="78856-103">建立備份電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="78856-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78856-104">句法</span><span class="sxs-lookup"><span data-stu-id="78856-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78856-105">說明</span><span class="sxs-lookup"><span data-stu-id="78856-105">DESCRIPTION</span></span>
<span data-ttu-id="78856-106">**新的-AzureRmBackupVault** Cmdlet 會建立 Azure 備份電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="78856-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="78856-107">這個 Cmdlet 會傳回 **AzureRmBackupVault** 物件，該物件充當 vault 實體的參照。</span><span class="sxs-lookup"><span data-stu-id="78856-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="78856-108">示例</span><span class="sxs-lookup"><span data-stu-id="78856-108">EXAMPLES</span></span>

### <span data-ttu-id="78856-109">範例1：建立備份電子倉庫</span><span class="sxs-lookup"><span data-stu-id="78856-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="78856-110">這個命令會建立名為 Vault03 的 Azure 備份電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="78856-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="78856-111">Vault 位於 [西部美國] 地區名為 [ResourceGroup01] 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="78856-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="78856-112">Vault 會使用預設的 GeoRedundant 儲存類型。</span><span class="sxs-lookup"><span data-stu-id="78856-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="78856-113">範例2：建立使用本機冗余儲存空間的備份電子倉庫</span><span class="sxs-lookup"><span data-stu-id="78856-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="78856-114">這個命令會建立名為 Vault03 的 Azure 備份電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="78856-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="78856-115">Vault 位於 [西部美國] 地區名為 [ResourceGroup02] 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="78856-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="78856-116">Vault 會使用 LocallyRedundant 儲存類型。</span><span class="sxs-lookup"><span data-stu-id="78856-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="78856-117">參數</span><span class="sxs-lookup"><span data-stu-id="78856-117">PARAMETERS</span></span>

### <span data-ttu-id="78856-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78856-118">-DefaultProfile</span></span>
<span data-ttu-id="78856-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="78856-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78856-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="78856-120">-Name</span></span>
<span data-ttu-id="78856-121">指定 Azure 備份保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="78856-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="78856-122">名稱在資源群組中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="78856-122">The name must be unique in a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78856-123">-Region</span><span class="sxs-lookup"><span data-stu-id="78856-123">-Region</span></span>
<span data-ttu-id="78856-124">指定備份保存庫所在的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="78856-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="78856-125">針對混合式備份案例，建議您在接近內部部署伺服器的區域中建立電子倉庫，以減少延遲。</span><span class="sxs-lookup"><span data-stu-id="78856-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="78856-126">若要將 Azure 基礎結構的備份做為服務 (IaaS) 虛擬機器，該保存庫就會成為本機虛擬機器的探索點。</span><span class="sxs-lookup"><span data-stu-id="78856-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78856-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78856-127">-ResourceGroupName</span></span>
<span data-ttu-id="78856-128">指定此 Cmdlet 建立備份電子倉庫之現有 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78856-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="78856-129">若要建立資源群組，請使用 New-AzureRMResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78856-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="78856-130">[資源] 群組和 [Azure 備份] 電子倉庫不需要位於同一個區域中。</span><span class="sxs-lookup"><span data-stu-id="78856-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78856-131">儲存空間</span><span class="sxs-lookup"><span data-stu-id="78856-131">-Storage</span></span>
<span data-ttu-id="78856-132">指定備份資料的儲存類型。</span><span class="sxs-lookup"><span data-stu-id="78856-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="78856-133">此參數可接受的值為： LocallyRedundant 和 GeoRedundant。</span><span class="sxs-lookup"><span data-stu-id="78856-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="78856-134">預設值為 GeoRedundant。</span><span class="sxs-lookup"><span data-stu-id="78856-134">The default value is GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78856-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78856-135">CommonParameters</span></span>
<span data-ttu-id="78856-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78856-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78856-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78856-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78856-138">輸入</span><span class="sxs-lookup"><span data-stu-id="78856-138">INPUTS</span></span>

### <span data-ttu-id="78856-139">所有</span><span class="sxs-lookup"><span data-stu-id="78856-139">None</span></span>

## <span data-ttu-id="78856-140">輸出</span><span class="sxs-lookup"><span data-stu-id="78856-140">OUTPUTS</span></span>

### <span data-ttu-id="78856-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="78856-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="78856-142">筆記</span><span class="sxs-lookup"><span data-stu-id="78856-142">NOTES</span></span>
* <span data-ttu-id="78856-143">所有</span><span class="sxs-lookup"><span data-stu-id="78856-143">None</span></span>

## <span data-ttu-id="78856-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="78856-144">RELATED LINKS</span></span>

[<span data-ttu-id="78856-145">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="78856-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="78856-146">移除-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="78856-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="78856-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="78856-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


