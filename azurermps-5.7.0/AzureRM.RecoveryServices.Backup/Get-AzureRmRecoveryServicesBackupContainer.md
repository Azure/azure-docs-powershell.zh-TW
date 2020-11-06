---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c861c9f18f2fb91838b8e527e2c3ee637098c00a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446143"
---
# <span data-ttu-id="6ce58-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6ce58-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="6ce58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ce58-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce58-103">取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="6ce58-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ce58-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ce58-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ce58-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ce58-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce58-106">**AzureRmRecoveryServicesBackupContainer** Cmdlet 會取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="6ce58-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="6ce58-107">備份容器封裝 modelled 為備份專案的資料來源。</span><span class="sxs-lookup"><span data-stu-id="6ce58-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="6ce58-108">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ce58-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6ce58-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ce58-109">EXAMPLES</span></span>

### <span data-ttu-id="6ce58-110">範例1：取得特定的容器</span><span class="sxs-lookup"><span data-stu-id="6ce58-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="6ce58-111">這個命令會取得名為 V2VM 類型的容器。</span><span class="sxs-lookup"><span data-stu-id="6ce58-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="6ce58-112">範例2：取得特定類型的所有容器</span><span class="sxs-lookup"><span data-stu-id="6ce58-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="6ce58-113">這個命令會取得所有由 Azure 備份代理程式保護的 Windows 容器。</span><span class="sxs-lookup"><span data-stu-id="6ce58-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="6ce58-114">只有 Windows 容器才需要 *BackupManagementType* 參數。</span><span class="sxs-lookup"><span data-stu-id="6ce58-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="6ce58-115">參數</span><span class="sxs-lookup"><span data-stu-id="6ce58-115">PARAMETERS</span></span>

### <span data-ttu-id="6ce58-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6ce58-116">-BackupManagementType</span></span>
<span data-ttu-id="6ce58-117">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="6ce58-117">Specifies the backup management type.</span></span>
<span data-ttu-id="6ce58-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6ce58-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ce58-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="6ce58-119">AzureVM</span></span>
- <span data-ttu-id="6ce58-120">MARS</span><span class="sxs-lookup"><span data-stu-id="6ce58-120">MARS</span></span>
- <span data-ttu-id="6ce58-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="6ce58-121">AzureSQL</span></span>

<span data-ttu-id="6ce58-122">這個參數可用來區分使用 MARS 代理程式或其他備份引擎備份的 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="6ce58-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce58-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="6ce58-123">-ContainerType</span></span>
<span data-ttu-id="6ce58-124">指定備份容器類型。</span><span class="sxs-lookup"><span data-stu-id="6ce58-124">Specifies the backup container type.</span></span>
<span data-ttu-id="6ce58-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6ce58-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ce58-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="6ce58-126">AzureVM</span></span> 
- <span data-ttu-id="6ce58-127">時間</span><span class="sxs-lookup"><span data-stu-id="6ce58-127">Windows</span></span>
- <span data-ttu-id="6ce58-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="6ce58-128">AzureSQL</span></span>

```yaml
Type: ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce58-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce58-129">-DefaultProfile</span></span>
<span data-ttu-id="6ce58-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ce58-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ce58-131">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6ce58-131">-FriendlyName</span></span>
<span data-ttu-id="6ce58-132">指定要取得之容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="6ce58-132">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce58-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ce58-133">-Name</span></span>
<span data-ttu-id="6ce58-134">指定要取得的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6ce58-134">Specifies the name of the container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce58-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce58-135">-ResourceGroupName</span></span>
<span data-ttu-id="6ce58-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ce58-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="6ce58-137">此參數僅適用于 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6ce58-137">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce58-138">-狀態</span><span class="sxs-lookup"><span data-stu-id="6ce58-138">-Status</span></span>
<span data-ttu-id="6ce58-139">指定容器註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="6ce58-139">Specifies the container registration status.</span></span>
<span data-ttu-id="6ce58-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6ce58-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ce58-141">已</span><span class="sxs-lookup"><span data-stu-id="6ce58-141">Registered</span></span>

```yaml
Type: ContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce58-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce58-142">CommonParameters</span></span>
<span data-ttu-id="6ce58-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ce58-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce58-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ce58-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce58-145">輸入</span><span class="sxs-lookup"><span data-stu-id="6ce58-145">INPUTS</span></span>

### <span data-ttu-id="6ce58-146">所有</span><span class="sxs-lookup"><span data-stu-id="6ce58-146">None</span></span>
<span data-ttu-id="6ce58-147">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6ce58-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ce58-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6ce58-148">OUTPUTS</span></span>

### <span data-ttu-id="6ce58-149">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="6ce58-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="6ce58-150">[System.object]. RecoveryServices [ContainerBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="6ce58-150">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="6ce58-151">筆記</span><span class="sxs-lookup"><span data-stu-id="6ce58-151">NOTES</span></span>

## <span data-ttu-id="6ce58-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ce58-152">RELATED LINKS</span></span>

[<span data-ttu-id="6ce58-153">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6ce58-153">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="6ce58-154">AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="6ce58-154">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="6ce58-155">取消註冊-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6ce58-155">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


