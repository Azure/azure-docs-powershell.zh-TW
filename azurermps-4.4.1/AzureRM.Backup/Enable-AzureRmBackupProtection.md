---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446882"
---
# <span data-ttu-id="1fd87-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1fd87-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="1fd87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fd87-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd87-103">將專案與 Azure 備份保護原則建立關聯。</span><span class="sxs-lookup"><span data-stu-id="1fd87-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fd87-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fd87-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fd87-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fd87-105">DESCRIPTION</span></span>
<span data-ttu-id="1fd87-106">**Enable-AzureRmBackupProtection** Cmdlet 會將專案與 Azure 備份保護原則建立關聯。</span><span class="sxs-lookup"><span data-stu-id="1fd87-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="1fd87-107">若要啟用保護原則，您必須先擁有現有的備份專案和現有的原則。</span><span class="sxs-lookup"><span data-stu-id="1fd87-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="1fd87-108">兩者必須屬於相同的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="1fd87-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="1fd87-109">[備份排程] 會針對專案及後續備份的增量複本進行完整的初始複本。</span><span class="sxs-lookup"><span data-stu-id="1fd87-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="1fd87-110">示例</span><span class="sxs-lookup"><span data-stu-id="1fd87-110">EXAMPLES</span></span>

### <span data-ttu-id="1fd87-111">範例1：在 Azure 虛擬機器上啟用保護</span><span class="sxs-lookup"><span data-stu-id="1fd87-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="1fd87-112">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="1fd87-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="1fd87-113">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="1fd87-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="1fd87-114">第二個命令會針對 $Vault 中的電子倉庫，取得名為 DefaultPolicy 的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="1fd87-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="1fd87-115">該命令會將該物件儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="1fd87-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="1fd87-116">最後一個命令會使用管線運算子，將一個 Cmdlet 的值傳遞到下一個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fd87-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="1fd87-117">它會使用 Get-AzureRmBackupContainer Cmdlet 來取得容器。</span><span class="sxs-lookup"><span data-stu-id="1fd87-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="1fd87-118">命令會使用 Get-AzureRmBackupItem Cmdlet 從該容器中取得備份專案。</span><span class="sxs-lookup"><span data-stu-id="1fd87-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="1fd87-119">目前的 Cmdlet 會針對命令傳遞到該 Cmdlet 的專案啟用 $Policy 中儲存的原則。</span><span class="sxs-lookup"><span data-stu-id="1fd87-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="1fd87-120">參數</span><span class="sxs-lookup"><span data-stu-id="1fd87-120">PARAMETERS</span></span>

### <span data-ttu-id="1fd87-121">-專案</span><span class="sxs-lookup"><span data-stu-id="1fd87-121">-Item</span></span>
<span data-ttu-id="1fd87-122">指定此 Cmdlet 針對其啟用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="1fd87-122">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="1fd87-123">若要取得 **AzureRmBackupItem** ，請使用 Get-AzureRmBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fd87-123">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd87-124">-原則</span><span class="sxs-lookup"><span data-stu-id="1fd87-124">-Policy</span></span>
<span data-ttu-id="1fd87-125">指定此 Cmdlet 與專案相關聯的保護原則。</span><span class="sxs-lookup"><span data-stu-id="1fd87-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="1fd87-126">若要取得 **AzureRmBackupProtectionPolicy** 物件，請使用 Get-AzureRmBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fd87-126">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd87-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd87-127">-DefaultProfile</span></span>
<span data-ttu-id="1fd87-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fd87-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fd87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd87-129">CommonParameters</span></span>
<span data-ttu-id="1fd87-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fd87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd87-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fd87-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd87-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1fd87-132">INPUTS</span></span>

### <span data-ttu-id="1fd87-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="1fd87-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="1fd87-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1fd87-134">OUTPUTS</span></span>

### <span data-ttu-id="1fd87-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="1fd87-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="1fd87-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1fd87-136">NOTES</span></span>

## <span data-ttu-id="1fd87-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fd87-137">RELATED LINKS</span></span>

[<span data-ttu-id="1fd87-138">備份-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="1fd87-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="1fd87-139">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="1fd87-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="1fd87-140">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fd87-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

