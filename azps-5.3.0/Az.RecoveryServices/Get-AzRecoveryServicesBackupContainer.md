---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 90532c6d314c78e6b7242ec480b95991138719de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439083"
---
# <span data-ttu-id="8d3a1-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8d3a1-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="8d3a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d3a1-102">SYNOPSIS</span></span>

<span data-ttu-id="8d3a1-103">取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-103">Gets Backup containers.</span></span>

## <span data-ttu-id="8d3a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d3a1-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d3a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d3a1-105">DESCRIPTION</span></span>

<span data-ttu-id="8d3a1-106">**AzRecoveryServicesBackupContainer** Cmdlet 會取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="8d3a1-107">備份容器封裝 modelled 為備份專案的資料來源。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="8d3a1-108">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="8d3a1-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d3a1-109">EXAMPLES</span></span>

### <span data-ttu-id="8d3a1-110">範例1：取得特定的容器</span><span class="sxs-lookup"><span data-stu-id="8d3a1-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="8d3a1-111">這個命令會取得名為 V2VM 類型的容器。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="8d3a1-112">範例2：取得特定類型的所有容器</span><span class="sxs-lookup"><span data-stu-id="8d3a1-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="8d3a1-113">這個命令會取得所有由 Azure 備份代理程式保護的 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="8d3a1-114">只有 Windows 容器才需要 **BackupManagementType** 參數。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="8d3a1-115">參數</span><span class="sxs-lookup"><span data-stu-id="8d3a1-115">PARAMETERS</span></span>

### <span data-ttu-id="8d3a1-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8d3a1-116">-BackupManagementType</span></span>

<span data-ttu-id="8d3a1-117">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-117">The class of resources being protected.</span></span> <span data-ttu-id="8d3a1-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8d3a1-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d3a1-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="8d3a1-119">AzureVM</span></span>
- <span data-ttu-id="8d3a1-120">MARS</span><span class="sxs-lookup"><span data-stu-id="8d3a1-120">MARS</span></span>
- <span data-ttu-id="8d3a1-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="8d3a1-121">AzureWorkload</span></span>
- <span data-ttu-id="8d3a1-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="8d3a1-122">AzureStorage</span></span>

<span data-ttu-id="8d3a1-123">這個參數可用來區分使用 MARS 代理程式或其他備份引擎備份的 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3a1-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="8d3a1-124">-ContainerType</span></span>

<span data-ttu-id="8d3a1-125">指定備份容器類型。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-125">Specifies the backup container type.</span></span>
<span data-ttu-id="8d3a1-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8d3a1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d3a1-127">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="8d3a1-127">AzureVM</span></span>
- <span data-ttu-id="8d3a1-128">時間</span><span class="sxs-lookup"><span data-stu-id="8d3a1-128">Windows</span></span>
- <span data-ttu-id="8d3a1-129">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="8d3a1-129">AzureStorage</span></span>
- <span data-ttu-id="8d3a1-130">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="8d3a1-130">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d3a1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d3a1-131">-DefaultProfile</span></span>

<span data-ttu-id="8d3a1-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d3a1-133">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8d3a1-133">-FriendlyName</span></span>

<span data-ttu-id="8d3a1-134">指定要取得之容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="8d3a1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d3a1-135">-ResourceGroupName</span></span>

<span data-ttu-id="8d3a1-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="8d3a1-137">此參數僅適用于 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="8d3a1-138">-狀態</span><span class="sxs-lookup"><span data-stu-id="8d3a1-138">-Status</span></span>

<span data-ttu-id="8d3a1-139">指定容器註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-139">Specifies the container registration status.</span></span>
<span data-ttu-id="8d3a1-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8d3a1-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d3a1-141">已</span><span class="sxs-lookup"><span data-stu-id="8d3a1-141">Registered</span></span>

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

### <span data-ttu-id="8d3a1-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8d3a1-142">-VaultId</span></span>

<span data-ttu-id="8d3a1-143">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8d3a1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d3a1-144">CommonParameters</span></span>
<span data-ttu-id="8d3a1-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d3a1-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d3a1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d3a1-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8d3a1-147">INPUTS</span></span>

### <span data-ttu-id="8d3a1-148">System.object</span><span class="sxs-lookup"><span data-stu-id="8d3a1-148">System.String</span></span>

## <span data-ttu-id="8d3a1-149">輸出</span><span class="sxs-lookup"><span data-stu-id="8d3a1-149">OUTPUTS</span></span>

### <span data-ttu-id="8d3a1-150">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="8d3a1-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="8d3a1-151">筆記</span><span class="sxs-lookup"><span data-stu-id="8d3a1-151">NOTES</span></span>

## <span data-ttu-id="8d3a1-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d3a1-152">RELATED LINKS</span></span>

[<span data-ttu-id="8d3a1-153">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8d3a1-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8d3a1-154">AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="8d3a1-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="8d3a1-155">取消註冊-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8d3a1-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
