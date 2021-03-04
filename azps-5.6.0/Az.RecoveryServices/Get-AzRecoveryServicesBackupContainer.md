---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0fb1df2d72259c6c0f427a9a66f4cf271cc0cbfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909994"
---
# <span data-ttu-id="83a26-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="83a26-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="83a26-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83a26-102">SYNOPSIS</span></span>

<span data-ttu-id="83a26-103">獲得備份容器。</span><span class="sxs-lookup"><span data-stu-id="83a26-103">Gets Backup containers.</span></span>

## <span data-ttu-id="83a26-104">語法</span><span class="sxs-lookup"><span data-stu-id="83a26-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83a26-105">描述</span><span class="sxs-lookup"><span data-stu-id="83a26-105">DESCRIPTION</span></span>

<span data-ttu-id="83a26-106">**Get-AzRecoveryServicesBackupContainer Cmdlet** 會取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="83a26-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="83a26-107">備份容器會封裝封裝成備份專案的資料來源。</span><span class="sxs-lookup"><span data-stu-id="83a26-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="83a26-108">針對容器類型 "Azure VM"，輸出會列出名稱與傳遞為 Friendly Name 參數值完全一樣的所有容器。</span><span class="sxs-lookup"><span data-stu-id="83a26-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="83a26-109">針對其他容器類型，輸出會提供名稱類似 Friendly 名稱參數傳遞值的容器清單。</span><span class="sxs-lookup"><span data-stu-id="83a26-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="83a26-110">使用 -VaultId 參數設定庫上下文。</span><span class="sxs-lookup"><span data-stu-id="83a26-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="83a26-111">例子</span><span class="sxs-lookup"><span data-stu-id="83a26-111">EXAMPLES</span></span>

### <span data-ttu-id="83a26-112">範例 1：取得特定容器</span><span class="sxs-lookup"><span data-stu-id="83a26-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="83a26-113">此命令會獲得類型為 Azure VM 的 V2 VM 容器。</span><span class="sxs-lookup"><span data-stu-id="83a26-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="83a26-114">範例 2：取得特定類型的所有容器</span><span class="sxs-lookup"><span data-stu-id="83a26-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="83a26-115">此命令會獲得受 Azure 備份代理程式保護的所有 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="83a26-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="83a26-116">只有 Windows 容器才需要 **BackupManagementType** 參數。</span><span class="sxs-lookup"><span data-stu-id="83a26-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="83a26-117">參數</span><span class="sxs-lookup"><span data-stu-id="83a26-117">PARAMETERS</span></span>

### <span data-ttu-id="83a26-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="83a26-118">-BackupManagementType</span></span>

<span data-ttu-id="83a26-119">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="83a26-119">The class of resources being protected.</span></span> <span data-ttu-id="83a26-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="83a26-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83a26-121">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="83a26-121">AzureVM</span></span>
- <span data-ttu-id="83a26-122">火星</span><span class="sxs-lookup"><span data-stu-id="83a26-122">MARS</span></span>
- <span data-ttu-id="83a26-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="83a26-123">AzureWorkload</span></span>
- <span data-ttu-id="83a26-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="83a26-124">AzureStorage</span></span>

<span data-ttu-id="83a26-125">此參數是用來區分使用 MARS 代理程式或其他備份引擎備份的 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="83a26-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="83a26-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="83a26-126">-ContainerType</span></span>

<span data-ttu-id="83a26-127">指定備份容器類型。</span><span class="sxs-lookup"><span data-stu-id="83a26-127">Specifies the backup container type.</span></span>
<span data-ttu-id="83a26-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="83a26-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83a26-129">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="83a26-129">AzureVM</span></span>
- <span data-ttu-id="83a26-130">窗戶</span><span class="sxs-lookup"><span data-stu-id="83a26-130">Windows</span></span>
- <span data-ttu-id="83a26-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="83a26-131">AzureStorage</span></span>
- <span data-ttu-id="83a26-132">AzureAZMAppContainer</span><span class="sxs-lookup"><span data-stu-id="83a26-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="83a26-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a26-133">-DefaultProfile</span></span>

<span data-ttu-id="83a26-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="83a26-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83a26-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="83a26-135">-FriendlyName</span></span>

<span data-ttu-id="83a26-136">指定要取得之容器的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="83a26-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="83a26-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83a26-137">-ResourceGroupName</span></span>

<span data-ttu-id="83a26-138">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a26-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="83a26-139">此參數僅適用于 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="83a26-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="83a26-140">-狀態</span><span class="sxs-lookup"><span data-stu-id="83a26-140">-Status</span></span>

<span data-ttu-id="83a26-141">指定容器註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="83a26-141">Specifies the container registration status.</span></span>
<span data-ttu-id="83a26-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="83a26-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83a26-143">註冊</span><span class="sxs-lookup"><span data-stu-id="83a26-143">Registered</span></span>

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

### <span data-ttu-id="83a26-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="83a26-144">-VaultId</span></span>

<span data-ttu-id="83a26-145">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="83a26-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="83a26-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a26-146">CommonParameters</span></span>
<span data-ttu-id="83a26-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83a26-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a26-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83a26-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a26-149">輸入</span><span class="sxs-lookup"><span data-stu-id="83a26-149">INPUTS</span></span>

### <span data-ttu-id="83a26-150">System.String</span><span class="sxs-lookup"><span data-stu-id="83a26-150">System.String</span></span>

## <span data-ttu-id="83a26-151">輸出</span><span class="sxs-lookup"><span data-stu-id="83a26-151">OUTPUTS</span></span>

### <span data-ttu-id="83a26-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="83a26-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="83a26-153">筆記</span><span class="sxs-lookup"><span data-stu-id="83a26-153">NOTES</span></span>

## <span data-ttu-id="83a26-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="83a26-154">RELATED LINKS</span></span>

[<span data-ttu-id="83a26-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="83a26-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="83a26-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="83a26-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="83a26-157">取消註冊-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="83a26-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
