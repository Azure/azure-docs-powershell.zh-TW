---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621160"
---
# <span data-ttu-id="da89a-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="da89a-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="da89a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da89a-102">SYNOPSIS</span></span>
<span data-ttu-id="da89a-103">取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="da89a-103">Gets Backup containers.</span></span>

## <span data-ttu-id="da89a-104">句法</span><span class="sxs-lookup"><span data-stu-id="da89a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da89a-105">說明</span><span class="sxs-lookup"><span data-stu-id="da89a-105">DESCRIPTION</span></span>
<span data-ttu-id="da89a-106">**AzRecoveryServicesBackupContainer** Cmdlet 會取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="da89a-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="da89a-107">備份容器封裝 modelled 為備份專案的資料來源。</span><span class="sxs-lookup"><span data-stu-id="da89a-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="da89a-108">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da89a-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="da89a-109">示例</span><span class="sxs-lookup"><span data-stu-id="da89a-109">EXAMPLES</span></span>

### <span data-ttu-id="da89a-110">範例1：取得特定的容器</span><span class="sxs-lookup"><span data-stu-id="da89a-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="da89a-111">這個命令會取得名為 V2VM 類型的容器。</span><span class="sxs-lookup"><span data-stu-id="da89a-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="da89a-112">範例2：取得特定類型的所有容器</span><span class="sxs-lookup"><span data-stu-id="da89a-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="da89a-113">這個命令會取得所有由 Azure 備份代理程式保護的 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="da89a-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="da89a-114">只有 Windows 容器才需要 *BackupManagementType* 參數。</span><span class="sxs-lookup"><span data-stu-id="da89a-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="da89a-115">參數</span><span class="sxs-lookup"><span data-stu-id="da89a-115">PARAMETERS</span></span>

### <span data-ttu-id="da89a-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="da89a-116">-BackupManagementType</span></span>
<span data-ttu-id="da89a-117">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="da89a-117">Specifies the backup management type.</span></span>
<span data-ttu-id="da89a-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="da89a-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da89a-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="da89a-119">AzureVM</span></span>
- <span data-ttu-id="da89a-120">MARS</span><span class="sxs-lookup"><span data-stu-id="da89a-120">MARS</span></span>
- <span data-ttu-id="da89a-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="da89a-121">AzureSQL</span></span>
- <span data-ttu-id="da89a-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="da89a-122">AzureStorage</span></span>

<span data-ttu-id="da89a-123">這個參數可用來區分使用 MARS 代理程式或其他備份引擎備份的 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="da89a-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="da89a-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="da89a-124">-ContainerType</span></span>
<span data-ttu-id="da89a-125">指定備份容器類型。</span><span class="sxs-lookup"><span data-stu-id="da89a-125">Specifies the backup container type.</span></span>
<span data-ttu-id="da89a-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="da89a-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da89a-127">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="da89a-127">AzureVM</span></span> 
- <span data-ttu-id="da89a-128">時間</span><span class="sxs-lookup"><span data-stu-id="da89a-128">Windows</span></span>
- <span data-ttu-id="da89a-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="da89a-129">AzureSQL</span></span>
- <span data-ttu-id="da89a-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="da89a-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da89a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da89a-131">-DefaultProfile</span></span>
<span data-ttu-id="da89a-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da89a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da89a-133">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="da89a-133">-FriendlyName</span></span>
<span data-ttu-id="da89a-134">指定要取得之容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="da89a-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="da89a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da89a-135">-ResourceGroupName</span></span>
<span data-ttu-id="da89a-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="da89a-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="da89a-137">此參數僅適用于 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="da89a-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="da89a-138">-狀態</span><span class="sxs-lookup"><span data-stu-id="da89a-138">-Status</span></span>
<span data-ttu-id="da89a-139">指定容器註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="da89a-139">Specifies the container registration status.</span></span>
<span data-ttu-id="da89a-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="da89a-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da89a-141">已</span><span class="sxs-lookup"><span data-stu-id="da89a-141">Registered</span></span>

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

### <span data-ttu-id="da89a-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="da89a-142">-VaultId</span></span>
<span data-ttu-id="da89a-143">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="da89a-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="da89a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da89a-144">CommonParameters</span></span>
<span data-ttu-id="da89a-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da89a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da89a-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da89a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da89a-147">輸入</span><span class="sxs-lookup"><span data-stu-id="da89a-147">INPUTS</span></span>

### <span data-ttu-id="da89a-148">System.object</span><span class="sxs-lookup"><span data-stu-id="da89a-148">System.String</span></span>

## <span data-ttu-id="da89a-149">輸出</span><span class="sxs-lookup"><span data-stu-id="da89a-149">OUTPUTS</span></span>

### <span data-ttu-id="da89a-150">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="da89a-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="da89a-151">筆記</span><span class="sxs-lookup"><span data-stu-id="da89a-151">NOTES</span></span>

## <span data-ttu-id="da89a-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="da89a-152">RELATED LINKS</span></span>

[<span data-ttu-id="da89a-153">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="da89a-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="da89a-154">AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="da89a-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="da89a-155">取消註冊-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="da89a-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

