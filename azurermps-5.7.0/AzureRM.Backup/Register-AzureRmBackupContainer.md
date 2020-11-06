---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 71c7d883994897e4dc4b450391fb50949a125c77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453155"
---
# <span data-ttu-id="c1812-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c1812-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="c1812-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1812-102">SYNOPSIS</span></span>
<span data-ttu-id="c1812-103">使用備份保存庫註冊容器。</span><span class="sxs-lookup"><span data-stu-id="c1812-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1812-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1812-104">SYNTAX</span></span>

### <span data-ttu-id="c1812-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="c1812-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1812-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="c1812-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1812-107">說明</span><span class="sxs-lookup"><span data-stu-id="c1812-107">DESCRIPTION</span></span>
<span data-ttu-id="c1812-108">**AzureRmBackupContainer** Cmdlet 會將容器註冊至 Azure 備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="c1812-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="c1812-109">若要使用 Azure 備份來設定備份，請先使用備份保存庫註冊您的伺服器或虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1812-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="c1812-110">這個 Cmdlet 會使用指定的保存庫，將基礎結構註冊為服務 (IaaS) 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1812-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="c1812-111">Register 操作會將 Azure 虛擬機器與備份保存庫進行關聯，並透過備份生命週期來追蹤虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c1812-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="c1812-112">示例</span><span class="sxs-lookup"><span data-stu-id="c1812-112">EXAMPLES</span></span>

### <span data-ttu-id="c1812-113">範例1：在備份保存庫中註冊虛擬機器</span><span class="sxs-lookup"><span data-stu-id="c1812-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="c1812-114">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="c1812-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="c1812-115">該命令會將電子倉庫儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="c1812-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="c1812-116">第二個命令會將名為 Contoso03Vm 的虛擬機器註冊到 $Vault 中的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="c1812-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="c1812-117">該虛擬機器屬於名為 ContosoService27 的服務。</span><span class="sxs-lookup"><span data-stu-id="c1812-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="c1812-118">參數</span><span class="sxs-lookup"><span data-stu-id="c1812-118">PARAMETERS</span></span>

### <span data-ttu-id="c1812-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1812-119">-DefaultProfile</span></span>
<span data-ttu-id="c1812-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c1812-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1812-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1812-121">-Name</span></span>
<span data-ttu-id="c1812-122">指定此 Cmdlet 註冊之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1812-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1812-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1812-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1812-124">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1812-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1812-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c1812-125">-ServiceName</span></span>
<span data-ttu-id="c1812-126">指定此 Cmdlet 註冊之虛擬機器的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c1812-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="c1812-127">通常，雲端服務名稱會有一個尾碼 cloudapp.net。</span><span class="sxs-lookup"><span data-stu-id="c1812-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="c1812-128">指定此參數時不要包含尾碼。</span><span class="sxs-lookup"><span data-stu-id="c1812-128">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="c1812-129">若要取得虛擬機器的相關資訊，請使用 Get-AzureRMVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1812-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="c1812-130">服務名稱是虛擬機器物件的 **DeploymentName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c1812-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1812-131">-保存庫</span><span class="sxs-lookup"><span data-stu-id="c1812-131">-Vault</span></span>
<span data-ttu-id="c1812-132">指定此 Cmdlet 註冊虛擬機器的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="c1812-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="c1812-133">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1812-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1812-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1812-134">CommonParameters</span></span>
<span data-ttu-id="c1812-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1812-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1812-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1812-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1812-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c1812-137">INPUTS</span></span>

### <span data-ttu-id="c1812-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c1812-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="c1812-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c1812-139">OUTPUTS</span></span>

### <span data-ttu-id="c1812-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="c1812-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="c1812-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c1812-141">NOTES</span></span>

## <span data-ttu-id="c1812-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1812-142">RELATED LINKS</span></span>

[<span data-ttu-id="c1812-143">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c1812-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


