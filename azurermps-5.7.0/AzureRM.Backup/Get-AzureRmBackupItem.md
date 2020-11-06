---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 892e9385a34f9c02ddcf41d57578bb320d645e0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457203"
---
# <span data-ttu-id="bc804-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc804-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="bc804-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc804-102">SYNOPSIS</span></span>
<span data-ttu-id="bc804-103">取得 [備份] 容器下的專案。</span><span class="sxs-lookup"><span data-stu-id="bc804-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc804-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc804-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc804-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc804-105">DESCRIPTION</span></span>
<span data-ttu-id="bc804-106">**AzureRmBackupItem** Cmdlet 會取得 Azure 備份中容器中的專案，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="bc804-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="bc804-107">使用 Enable-AzureRmBackupProtection Cmdlet 來啟用保護專案。</span><span class="sxs-lookup"><span data-stu-id="bc804-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="bc804-108">已登錄至備份保存庫的容器可以有一個或多個可以受到保護的專案。</span><span class="sxs-lookup"><span data-stu-id="bc804-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="bc804-109">針對 Azure 虛擬機器，虛擬機器容器中只能有一個專案。</span><span class="sxs-lookup"><span data-stu-id="bc804-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="bc804-110">示例</span><span class="sxs-lookup"><span data-stu-id="bc804-110">EXAMPLES</span></span>

### <span data-ttu-id="bc804-111">範例1：取得容器中的專案</span><span class="sxs-lookup"><span data-stu-id="bc804-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="bc804-112">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="bc804-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="bc804-113">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="bc804-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="bc804-114">第二個命令會在 $Vault 中使用 **AzureRmBackupContainer** Cmdlet，透過電子倉庫中的指定名稱取得容器。</span><span class="sxs-lookup"><span data-stu-id="bc804-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="bc804-115">該命令會將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="bc804-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="bc804-116">最後一個命令會在 $Container 的容器中取得備份專案。</span><span class="sxs-lookup"><span data-stu-id="bc804-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="bc804-117">範例2：查看專案的所有屬性</span><span class="sxs-lookup"><span data-stu-id="bc804-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="bc804-118">這個命令會在 $Container 中取得容器中的備份專案，然後將它傳送到 Select-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc804-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="bc804-119">該 Cmdlet 會傳回備份專案的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="bc804-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="bc804-120">如需詳細資訊，請輸入 `Get-Help Select-Object` 。</span><span class="sxs-lookup"><span data-stu-id="bc804-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="bc804-121">參數</span><span class="sxs-lookup"><span data-stu-id="bc804-121">PARAMETERS</span></span>

### <span data-ttu-id="bc804-122">-容器</span><span class="sxs-lookup"><span data-stu-id="bc804-122">-Container</span></span>
<span data-ttu-id="bc804-123">指定此 Cmdlet 取得備份專案的容器物件。</span><span class="sxs-lookup"><span data-stu-id="bc804-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="bc804-124">若要取得 **AzureRmBackupContainer** ，請使用 Get-AzureRmBackupContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc804-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc804-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc804-125">-DefaultProfile</span></span>
<span data-ttu-id="bc804-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bc804-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc804-127">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="bc804-127">-ProtectionStatus</span></span>
<span data-ttu-id="bc804-128">指定容器中某個專案的整體保護狀態。</span><span class="sxs-lookup"><span data-stu-id="bc804-128">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="bc804-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bc804-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc804-130">受</span><span class="sxs-lookup"><span data-stu-id="bc804-130">Protected</span></span> 
- <span data-ttu-id="bc804-131">從而</span><span class="sxs-lookup"><span data-stu-id="bc804-131">Protecting</span></span>  
- <span data-ttu-id="bc804-132">NotProtected</span><span class="sxs-lookup"><span data-stu-id="bc804-132">NotProtected</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc804-133">-狀態</span><span class="sxs-lookup"><span data-stu-id="bc804-133">-Status</span></span>
<span data-ttu-id="bc804-134">指定專案的備份狀態。</span><span class="sxs-lookup"><span data-stu-id="bc804-134">Specifies the backup status for an item.</span></span>
<span data-ttu-id="bc804-135">此參數可接受的值為： IRPending、Protected、ProtectionError 和 ProtectionStopped。</span><span class="sxs-lookup"><span data-stu-id="bc804-135">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="bc804-136">如果 *ProtectionStatus* 參數的值受保護，您可以使用 *Status* 參數值來篩選項目。</span><span class="sxs-lookup"><span data-stu-id="bc804-136">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc804-137">-類型</span><span class="sxs-lookup"><span data-stu-id="bc804-137">-Type</span></span>
<span data-ttu-id="bc804-138">指定此 Cmdlet 取得的專案類型。</span><span class="sxs-lookup"><span data-stu-id="bc804-138">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="bc804-139">目前唯一支援的值為 Add-azurevm。</span><span class="sxs-lookup"><span data-stu-id="bc804-139">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc804-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc804-140">CommonParameters</span></span>
<span data-ttu-id="bc804-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc804-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc804-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc804-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc804-143">輸入</span><span class="sxs-lookup"><span data-stu-id="bc804-143">INPUTS</span></span>

### <span data-ttu-id="bc804-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bc804-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="bc804-145">輸出</span><span class="sxs-lookup"><span data-stu-id="bc804-145">OUTPUTS</span></span>

### <span data-ttu-id="bc804-146">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc804-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="bc804-147">筆記</span><span class="sxs-lookup"><span data-stu-id="bc804-147">NOTES</span></span>

## <span data-ttu-id="bc804-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc804-148">RELATED LINKS</span></span>

[<span data-ttu-id="bc804-149">備份-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc804-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="bc804-150">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="bc804-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="bc804-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="bc804-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="bc804-152">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bc804-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="bc804-153">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="bc804-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="bc804-154">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc804-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


