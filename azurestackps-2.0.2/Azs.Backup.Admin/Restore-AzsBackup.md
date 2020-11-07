---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968485"
---
# <span data-ttu-id="5a35b-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="5a35b-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="5a35b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a35b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a35b-103">還原備份。</span><span class="sxs-lookup"><span data-stu-id="5a35b-103">Restore a backup.</span></span>

## <span data-ttu-id="5a35b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a35b-104">SYNTAX</span></span>

### <span data-ttu-id="5a35b-105">RestoreExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5a35b-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5a35b-106">還原</span><span class="sxs-lookup"><span data-stu-id="5a35b-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a35b-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5a35b-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5a35b-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5a35b-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a35b-109">說明</span><span class="sxs-lookup"><span data-stu-id="5a35b-109">DESCRIPTION</span></span>
<span data-ttu-id="5a35b-110">還原備份。</span><span class="sxs-lookup"><span data-stu-id="5a35b-110">Restore a backup.</span></span>

## <span data-ttu-id="5a35b-111">示例</span><span class="sxs-lookup"><span data-stu-id="5a35b-111">EXAMPLES</span></span>

### <span data-ttu-id="5a35b-112">範例1：還原備份</span><span class="sxs-lookup"><span data-stu-id="5a35b-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="5a35b-113">從 Azure 堆疊備份還原。</span><span class="sxs-lookup"><span data-stu-id="5a35b-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="5a35b-114">參數</span><span class="sxs-lookup"><span data-stu-id="5a35b-114">PARAMETERS</span></span>

### <span data-ttu-id="5a35b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a35b-115">-AsJob</span></span>
<span data-ttu-id="5a35b-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="5a35b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5a35b-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="5a35b-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="5a35b-118">解密憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="5a35b-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="5a35b-119">-DecryptionCertPath</span></span>
<span data-ttu-id="5a35b-120">解密憑證檔案的路徑，其私密金鑰 ( .pfx) 。</span><span class="sxs-lookup"><span data-stu-id="5a35b-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a35b-121">-DefaultProfile</span></span>
<span data-ttu-id="5a35b-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a35b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5a35b-123">-Force</span></span>
<span data-ttu-id="5a35b-124">不要求確認</span><span class="sxs-lookup"><span data-stu-id="5a35b-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="5a35b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a35b-125">-InputObject</span></span>
<span data-ttu-id="5a35b-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a35b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-127">-位置</span><span class="sxs-lookup"><span data-stu-id="5a35b-127">-Location</span></span>
<span data-ttu-id="5a35b-128">備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a35b-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a35b-129">-Name</span></span>
<span data-ttu-id="5a35b-130">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a35b-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a35b-131">-NoWait</span></span>
<span data-ttu-id="5a35b-132">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="5a35b-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5a35b-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a35b-133">-PassThru</span></span>
<span data-ttu-id="5a35b-134">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="5a35b-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5a35b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a35b-135">-ResourceGroupName</span></span>
<span data-ttu-id="5a35b-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a35b-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="5a35b-137">-RestoreOption</span></span>
<span data-ttu-id="5a35b-138">[還原選項] 的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a35b-138">Properties for restore options.</span></span>
<span data-ttu-id="5a35b-139">若要建立，請參閱 RESTOREOPTION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="5a35b-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-140">-擁有方</span><span class="sxs-lookup"><span data-stu-id="5a35b-140">-RoleName</span></span>
<span data-ttu-id="5a35b-141">要還原的 Azure 堆疊角色名稱，針對所有結構角色將它設為空白</span><span class="sxs-lookup"><span data-stu-id="5a35b-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a35b-142">-SubscriptionId</span></span>
<span data-ttu-id="5a35b-143">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5a35b-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5a35b-144">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5a35b-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5a35b-145">-確認</span><span class="sxs-lookup"><span data-stu-id="5a35b-145">-Confirm</span></span>
<span data-ttu-id="5a35b-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a35b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a35b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a35b-147">-WhatIf</span></span>
<span data-ttu-id="5a35b-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a35b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a35b-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a35b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a35b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a35b-150">CommonParameters</span></span>
<span data-ttu-id="5a35b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a35b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a35b-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a35b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a35b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="5a35b-153">INPUTS</span></span>

### <span data-ttu-id="5a35b-154">IBackupAdminIdentity （BackupAdmin）的</span><span class="sxs-lookup"><span data-stu-id="5a35b-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="5a35b-155">輸出</span><span class="sxs-lookup"><span data-stu-id="5a35b-155">OUTPUTS</span></span>

### <span data-ttu-id="5a35b-156">System.object</span><span class="sxs-lookup"><span data-stu-id="5a35b-156">System.Boolean</span></span>



## <span data-ttu-id="5a35b-157">筆記</span><span class="sxs-lookup"><span data-stu-id="5a35b-157">NOTES</span></span>

<span data-ttu-id="5a35b-158">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5a35b-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a35b-159">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5a35b-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5a35b-160">INPUTOBJECT <IBackupAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5a35b-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a35b-161">`[Backup <String>]`：備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a35b-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="5a35b-162">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5a35b-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a35b-163">`[Location <String>]`：備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a35b-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="5a35b-164">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a35b-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5a35b-165">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5a35b-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5a35b-166">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5a35b-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="5a35b-167">RESTOREOPTION <IRestoreOptions> ：還原選項的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a35b-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="5a35b-168">`[DecryptionCertBase64 <String>]`：以 Base64 字串的憑證檔案原始資料。</span><span class="sxs-lookup"><span data-stu-id="5a35b-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="5a35b-169">這應該是具有私用金鑰的 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="5a35b-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="5a35b-170">`[DecryptionCertPassword <String>]`：解密憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="5a35b-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="5a35b-171">`[RoleName <String>]`：用於還原的 Azure 堆疊角色名稱，針對所有結構角色將它設為空白</span><span class="sxs-lookup"><span data-stu-id="5a35b-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="5a35b-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a35b-172">RELATED LINKS</span></span>

