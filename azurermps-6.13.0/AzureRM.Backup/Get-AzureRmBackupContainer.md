---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623938"
---
# <span data-ttu-id="efd19-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="efd19-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="efd19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efd19-102">SYNOPSIS</span></span>
<span data-ttu-id="efd19-103">取得備份容器。</span><span class="sxs-lookup"><span data-stu-id="efd19-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efd19-104">句法</span><span class="sxs-lookup"><span data-stu-id="efd19-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efd19-105">說明</span><span class="sxs-lookup"><span data-stu-id="efd19-105">DESCRIPTION</span></span>
<span data-ttu-id="efd19-106">**AzureRmBackupContainer** Cmdlet 會取得 Azure 備份容器。</span><span class="sxs-lookup"><span data-stu-id="efd19-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>
<span data-ttu-id="efd19-107">**AzureBackupContainer** 封裝資料來源、受保護的專案和復原點。</span><span class="sxs-lookup"><span data-stu-id="efd19-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="efd19-108">**AzureBackupContainer** 可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="efd19-108">An **AzureBackupContainer** can be one of the following:</span></span> 
- <span data-ttu-id="efd19-109">Windows Server 電腦</span><span class="sxs-lookup"><span data-stu-id="efd19-109">A Windows Server computer</span></span>
- <span data-ttu-id="efd19-110">系統中心資料保護管理員 (SCDPM) 伺服器</span><span class="sxs-lookup"><span data-stu-id="efd19-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="efd19-111">將 Azure 基礎結構做為服務 (IaaS) 虛擬機器，然後備份才能備份資料來源或專案，您就必須使用 Azure 備份服務註冊容納該檔案的容器。</span><span class="sxs-lookup"><span data-stu-id="efd19-111">An Azure infrastructure as a service (IaaS) virtual machine Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="efd19-112">容器必須經過驗證，才能將備份資料傳送到備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="efd19-112">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="efd19-113">若是 Windows Server 電腦和 SCDPM 服務器，則會以伺服器的完整功能變數名稱保留註冊。</span><span class="sxs-lookup"><span data-stu-id="efd19-113">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="efd19-114">示例</span><span class="sxs-lookup"><span data-stu-id="efd19-114">EXAMPLES</span></span>

### <span data-ttu-id="efd19-115">範例1：查看已登錄到保存庫的所有伺服器</span><span class="sxs-lookup"><span data-stu-id="efd19-115">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="efd19-116">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="efd19-116">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="efd19-117">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="efd19-117">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="efd19-118">第二個命令會從 $Vault 中的電子倉庫中，取得類型為 Windows 的所有容器。</span><span class="sxs-lookup"><span data-stu-id="efd19-118">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="efd19-119">範例2：取得特定的容器</span><span class="sxs-lookup"><span data-stu-id="efd19-119">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="efd19-120">這個命令會取得名為 DPMSERVER 的容器。CONTOSO.COM。</span><span class="sxs-lookup"><span data-stu-id="efd19-120">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="efd19-121">此命令會指定 $Vault 和容器類型中的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="efd19-121">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="efd19-122">範例3：查看所有已註冊的 Azure 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="efd19-122">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="efd19-123">這個命令會從 $Vault 中的電子倉庫中取得已註冊的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="efd19-123">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="efd19-124">參數</span><span class="sxs-lookup"><span data-stu-id="efd19-124">PARAMETERS</span></span>

### <span data-ttu-id="efd19-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd19-125">-DefaultProfile</span></span>
<span data-ttu-id="efd19-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="efd19-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efd19-127">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd19-127">-ManagedResourceGroupName</span></span>
<span data-ttu-id="efd19-128">指定與容器相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efd19-128">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="efd19-129">這個名稱與您為 Register-AzureRmBackupContainer Cmdlet 的 *ServiceName* 或 *ResourceGroupName* 參數指定的值相同。</span><span class="sxs-lookup"><span data-stu-id="efd19-129">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd19-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="efd19-130">-Name</span></span>
<span data-ttu-id="efd19-131">指定此 Cmdlet 所取得之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="efd19-131">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd19-132">-狀態</span><span class="sxs-lookup"><span data-stu-id="efd19-132">-Status</span></span>
<span data-ttu-id="efd19-133">指定此 Cmdlet 取得之容器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="efd19-133">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="efd19-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="efd19-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efd19-135">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="efd19-135">NotRegistered</span></span> 
- <span data-ttu-id="efd19-136">已</span><span class="sxs-lookup"><span data-stu-id="efd19-136">Registered</span></span> 
- <span data-ttu-id="efd19-137">登錄</span><span class="sxs-lookup"><span data-stu-id="efd19-137">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd19-138">-類型</span><span class="sxs-lookup"><span data-stu-id="efd19-138">-Type</span></span>
<span data-ttu-id="efd19-139">指定此 Cmdlet 取得的容器類型。</span><span class="sxs-lookup"><span data-stu-id="efd19-139">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd19-140">-保存庫</span><span class="sxs-lookup"><span data-stu-id="efd19-140">-Vault</span></span>
<span data-ttu-id="efd19-141">指定此 Cmdlet 取得容器的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="efd19-141">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="efd19-142">若要取得 **AzureRmBackupVault** ，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efd19-142">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efd19-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd19-143">CommonParameters</span></span>
<span data-ttu-id="efd19-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efd19-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd19-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efd19-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd19-146">輸入</span><span class="sxs-lookup"><span data-stu-id="efd19-146">INPUTS</span></span>

### <span data-ttu-id="efd19-147">AzureRMBackupVault 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="efd19-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="efd19-148">參數：保存庫 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="efd19-148">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="efd19-149">輸出</span><span class="sxs-lookup"><span data-stu-id="efd19-149">OUTPUTS</span></span>

### <span data-ttu-id="efd19-150">AzureRMBackupContainer 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="efd19-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>

## <span data-ttu-id="efd19-151">筆記</span><span class="sxs-lookup"><span data-stu-id="efd19-151">NOTES</span></span>
* <span data-ttu-id="efd19-152">所有</span><span class="sxs-lookup"><span data-stu-id="efd19-152">None</span></span>

## <span data-ttu-id="efd19-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="efd19-153">RELATED LINKS</span></span>

[<span data-ttu-id="efd19-154">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="efd19-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="efd19-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="efd19-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="efd19-156">取消註冊-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="efd19-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


