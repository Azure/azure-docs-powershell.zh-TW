---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: 82e86d27c5ef628e6cd6122fa024ac72788e79db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452599"
---
# <span data-ttu-id="76a20-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="76a20-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="76a20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76a20-102">SYNOPSIS</span></span>
<span data-ttu-id="76a20-103">變更備份電子倉庫的儲存類型。</span><span class="sxs-lookup"><span data-stu-id="76a20-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76a20-104">句法</span><span class="sxs-lookup"><span data-stu-id="76a20-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a20-105">說明</span><span class="sxs-lookup"><span data-stu-id="76a20-105">DESCRIPTION</span></span>
<span data-ttu-id="76a20-106">**AzureRmBackupVault** Cmdlet 會變更 Azure 備份電子倉庫的儲存類型。</span><span class="sxs-lookup"><span data-stu-id="76a20-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="76a20-107">您無法修改電子倉庫的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="76a20-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="76a20-108">示例</span><span class="sxs-lookup"><span data-stu-id="76a20-108">EXAMPLES</span></span>

### <span data-ttu-id="76a20-109">範例1：變更現有電子倉庫的儲存空間</span><span class="sxs-lookup"><span data-stu-id="76a20-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="76a20-110">此命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的 Azure 備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="76a20-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="76a20-111">命令會使用管線運算子，將該電子倉庫傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76a20-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="76a20-112">目前的 Cmdlet 會將儲存類型變更為 LocallyRedundant。</span><span class="sxs-lookup"><span data-stu-id="76a20-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="76a20-113">參數</span><span class="sxs-lookup"><span data-stu-id="76a20-113">PARAMETERS</span></span>

### <span data-ttu-id="76a20-114">儲存空間</span><span class="sxs-lookup"><span data-stu-id="76a20-114">-Storage</span></span>
<span data-ttu-id="76a20-115">指定備份資料的儲存類型。</span><span class="sxs-lookup"><span data-stu-id="76a20-115">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="76a20-116">此參數可接受的值為： LocallyRedundant 和 GeoRedundant。</span><span class="sxs-lookup"><span data-stu-id="76a20-116">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a20-117">-保存庫</span><span class="sxs-lookup"><span data-stu-id="76a20-117">-Vault</span></span>
<span data-ttu-id="76a20-118">指定此 Cmdlet 修改的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="76a20-118">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="76a20-119">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76a20-119">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="76a20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a20-120">-DefaultProfile</span></span>
<span data-ttu-id="76a20-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76a20-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76a20-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a20-122">CommonParameters</span></span>
<span data-ttu-id="76a20-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76a20-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a20-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76a20-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a20-125">輸入</span><span class="sxs-lookup"><span data-stu-id="76a20-125">INPUTS</span></span>

### <span data-ttu-id="76a20-126">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="76a20-126">AzureRmBackupVault</span></span>

## <span data-ttu-id="76a20-127">輸出</span><span class="sxs-lookup"><span data-stu-id="76a20-127">OUTPUTS</span></span>

### <span data-ttu-id="76a20-128">所有</span><span class="sxs-lookup"><span data-stu-id="76a20-128">None</span></span>

## <span data-ttu-id="76a20-129">筆記</span><span class="sxs-lookup"><span data-stu-id="76a20-129">NOTES</span></span>
* <span data-ttu-id="76a20-130">當您註冊電子倉庫的第一台伺服器或虛擬機器時，儲存類型是 [已鎖定]。</span><span class="sxs-lookup"><span data-stu-id="76a20-130">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="76a20-131">接著，您無法變更儲存類型。</span><span class="sxs-lookup"><span data-stu-id="76a20-131">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="76a20-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="76a20-132">RELATED LINKS</span></span>

[<span data-ttu-id="76a20-133">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="76a20-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="76a20-134">新-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="76a20-134">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="76a20-135">移除-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="76a20-135">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


