---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: bd4945436c840323121be7a4450a0042acf67cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130983"
---
# <span data-ttu-id="0a61d-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0a61d-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="0a61d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a61d-102">SYNOPSIS</span></span>

<span data-ttu-id="0a61d-103">取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="0a61d-103">Gets Backup containers.</span></span>

## <span data-ttu-id="0a61d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a61d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a61d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a61d-105">DESCRIPTION</span></span>

<span data-ttu-id="0a61d-106">**AzRecoveryServicesBackupContainer** Cmdlet 會取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="0a61d-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="0a61d-107">備份容器封裝 modelled 為備份專案的資料來源。</span><span class="sxs-lookup"><span data-stu-id="0a61d-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="0a61d-108">針對容器類型 "Azure VM"，輸出會列出其名稱與以易記名稱參數值傳遞之完全相符的所有容器。</span><span class="sxs-lookup"><span data-stu-id="0a61d-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="0a61d-109">針對其他容器類型，輸出會提供名稱與為易記名稱參數傳遞的值類似的容器清單。</span><span class="sxs-lookup"><span data-stu-id="0a61d-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="0a61d-110">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="0a61d-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="0a61d-111">示例</span><span class="sxs-lookup"><span data-stu-id="0a61d-111">EXAMPLES</span></span>

### <span data-ttu-id="0a61d-112">範例1：取得特定的容器</span><span class="sxs-lookup"><span data-stu-id="0a61d-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="0a61d-113">這個命令會取得名為 V2VM 類型的容器。</span><span class="sxs-lookup"><span data-stu-id="0a61d-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="0a61d-114">範例2：取得特定類型的所有容器</span><span class="sxs-lookup"><span data-stu-id="0a61d-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="0a61d-115">這個命令會取得所有由 Azure 備份代理程式保護的 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="0a61d-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="0a61d-116">只有 Windows 容器才需要 **BackupManagementType** 參數。</span><span class="sxs-lookup"><span data-stu-id="0a61d-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="0a61d-117">參數</span><span class="sxs-lookup"><span data-stu-id="0a61d-117">PARAMETERS</span></span>

### <span data-ttu-id="0a61d-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0a61d-118">-BackupManagementType</span></span>

<span data-ttu-id="0a61d-119">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="0a61d-119">The class of resources being protected.</span></span> <span data-ttu-id="0a61d-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0a61d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a61d-121">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0a61d-121">AzureVM</span></span>
- <span data-ttu-id="0a61d-122">MARS</span><span class="sxs-lookup"><span data-stu-id="0a61d-122">MARS</span></span>
- <span data-ttu-id="0a61d-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="0a61d-123">AzureWorkload</span></span>
- <span data-ttu-id="0a61d-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0a61d-124">AzureStorage</span></span>

<span data-ttu-id="0a61d-125">這個參數可用來區分使用 MARS 代理程式或其他備份引擎備份的 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="0a61d-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="0a61d-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="0a61d-126">-ContainerType</span></span>

<span data-ttu-id="0a61d-127">指定備份容器類型。</span><span class="sxs-lookup"><span data-stu-id="0a61d-127">Specifies the backup container type.</span></span>
<span data-ttu-id="0a61d-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0a61d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a61d-129">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0a61d-129">AzureVM</span></span>
- <span data-ttu-id="0a61d-130">時間</span><span class="sxs-lookup"><span data-stu-id="0a61d-130">Windows</span></span>
- <span data-ttu-id="0a61d-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0a61d-131">AzureStorage</span></span>
- <span data-ttu-id="0a61d-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="0a61d-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="0a61d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a61d-133">-DefaultProfile</span></span>

<span data-ttu-id="0a61d-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a61d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a61d-135">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0a61d-135">-FriendlyName</span></span>

<span data-ttu-id="0a61d-136">指定要取得之容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0a61d-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="0a61d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a61d-137">-ResourceGroupName</span></span>

<span data-ttu-id="0a61d-138">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a61d-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="0a61d-139">此參數僅適用于 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0a61d-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="0a61d-140">-狀態</span><span class="sxs-lookup"><span data-stu-id="0a61d-140">-Status</span></span>

<span data-ttu-id="0a61d-141">指定容器註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="0a61d-141">Specifies the container registration status.</span></span>
<span data-ttu-id="0a61d-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0a61d-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a61d-143">已</span><span class="sxs-lookup"><span data-stu-id="0a61d-143">Registered</span></span>

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

### <span data-ttu-id="0a61d-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0a61d-144">-VaultId</span></span>

<span data-ttu-id="0a61d-145">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="0a61d-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0a61d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a61d-146">CommonParameters</span></span>
<span data-ttu-id="0a61d-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a61d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a61d-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a61d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a61d-149">輸入</span><span class="sxs-lookup"><span data-stu-id="0a61d-149">INPUTS</span></span>

### <span data-ttu-id="0a61d-150">System.object</span><span class="sxs-lookup"><span data-stu-id="0a61d-150">System.String</span></span>

## <span data-ttu-id="0a61d-151">輸出</span><span class="sxs-lookup"><span data-stu-id="0a61d-151">OUTPUTS</span></span>

### <span data-ttu-id="0a61d-152">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="0a61d-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="0a61d-153">筆記</span><span class="sxs-lookup"><span data-stu-id="0a61d-153">NOTES</span></span>

## <span data-ttu-id="0a61d-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a61d-154">RELATED LINKS</span></span>

[<span data-ttu-id="0a61d-155">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0a61d-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0a61d-156">AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0a61d-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="0a61d-157">取消註冊-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0a61d-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
