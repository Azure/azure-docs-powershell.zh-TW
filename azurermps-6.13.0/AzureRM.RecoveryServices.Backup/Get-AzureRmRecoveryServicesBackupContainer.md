---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625263"
---
# <span data-ttu-id="46d4b-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="46d4b-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="46d4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="46d4b-103">取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="46d4b-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46d4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="46d4b-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46d4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="46d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="46d4b-106">**AzureRmRecoveryServicesBackupContainer** Cmdlet 會取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="46d4b-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="46d4b-107">備份容器封裝 modelled 為備份專案的資料來源。</span><span class="sxs-lookup"><span data-stu-id="46d4b-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="46d4b-108">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46d4b-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="46d4b-109">示例</span><span class="sxs-lookup"><span data-stu-id="46d4b-109">EXAMPLES</span></span>

### <span data-ttu-id="46d4b-110">範例1：取得特定的容器</span><span class="sxs-lookup"><span data-stu-id="46d4b-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="46d4b-111">這個命令會取得名為 V2VM 類型的容器。</span><span class="sxs-lookup"><span data-stu-id="46d4b-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="46d4b-112">範例2：取得特定類型的所有容器</span><span class="sxs-lookup"><span data-stu-id="46d4b-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="46d4b-113">這個命令會取得所有由 Azure 備份代理程式保護的 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="46d4b-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="46d4b-114">只有 Windows 容器才需要 *BackupManagementType* 參數。</span><span class="sxs-lookup"><span data-stu-id="46d4b-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="46d4b-115">參數</span><span class="sxs-lookup"><span data-stu-id="46d4b-115">PARAMETERS</span></span>

### <span data-ttu-id="46d4b-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="46d4b-116">-BackupManagementType</span></span>
<span data-ttu-id="46d4b-117">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="46d4b-117">Specifies the backup management type.</span></span>
<span data-ttu-id="46d4b-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="46d4b-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46d4b-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="46d4b-119">AzureVM</span></span>
- <span data-ttu-id="46d4b-120">MARS</span><span class="sxs-lookup"><span data-stu-id="46d4b-120">MARS</span></span>
- <span data-ttu-id="46d4b-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="46d4b-121">AzureSQL</span></span>
- <span data-ttu-id="46d4b-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="46d4b-122">AzureStorage</span></span>

<span data-ttu-id="46d4b-123">這個參數可用來區分使用 MARS 代理程式或其他備份引擎備份的 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="46d4b-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4b-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="46d4b-124">-ContainerType</span></span>
<span data-ttu-id="46d4b-125">指定備份容器類型。</span><span class="sxs-lookup"><span data-stu-id="46d4b-125">Specifies the backup container type.</span></span>
<span data-ttu-id="46d4b-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="46d4b-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46d4b-127">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="46d4b-127">AzureVM</span></span> 
- <span data-ttu-id="46d4b-128">時間</span><span class="sxs-lookup"><span data-stu-id="46d4b-128">Windows</span></span>
- <span data-ttu-id="46d4b-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="46d4b-129">AzureSQL</span></span>
- <span data-ttu-id="46d4b-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="46d4b-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d4b-131">-DefaultProfile</span></span>
<span data-ttu-id="46d4b-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46d4b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46d4b-133">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="46d4b-133">-FriendlyName</span></span>
<span data-ttu-id="46d4b-134">指定要取得之容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="46d4b-134">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4b-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="46d4b-135">-Name</span></span>
<span data-ttu-id="46d4b-136">指定要取得的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="46d4b-136">Specifies the name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d4b-137">-ResourceGroupName</span></span>
<span data-ttu-id="46d4b-138">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46d4b-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="46d4b-139">此參數僅適用于 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="46d4b-139">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4b-140">-狀態</span><span class="sxs-lookup"><span data-stu-id="46d4b-140">-Status</span></span>
<span data-ttu-id="46d4b-141">指定容器註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="46d4b-141">Specifies the container registration status.</span></span>
<span data-ttu-id="46d4b-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="46d4b-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46d4b-143">已</span><span class="sxs-lookup"><span data-stu-id="46d4b-143">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4b-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="46d4b-144">-VaultId</span></span>
<span data-ttu-id="46d4b-145">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="46d4b-145">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d4b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d4b-146">CommonParameters</span></span>
<span data-ttu-id="46d4b-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46d4b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d4b-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46d4b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d4b-149">輸入</span><span class="sxs-lookup"><span data-stu-id="46d4b-149">INPUTS</span></span>

### <span data-ttu-id="46d4b-150">System.object</span><span class="sxs-lookup"><span data-stu-id="46d4b-150">System.String</span></span>
<span data-ttu-id="46d4b-151">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="46d4b-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="46d4b-152">輸出</span><span class="sxs-lookup"><span data-stu-id="46d4b-152">OUTPUTS</span></span>

### <span data-ttu-id="46d4b-153">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="46d4b-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="46d4b-154">筆記</span><span class="sxs-lookup"><span data-stu-id="46d4b-154">NOTES</span></span>

## <span data-ttu-id="46d4b-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="46d4b-155">RELATED LINKS</span></span>

[<span data-ttu-id="46d4b-156">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="46d4b-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="46d4b-157">AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="46d4b-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="46d4b-158">取消註冊-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="46d4b-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


