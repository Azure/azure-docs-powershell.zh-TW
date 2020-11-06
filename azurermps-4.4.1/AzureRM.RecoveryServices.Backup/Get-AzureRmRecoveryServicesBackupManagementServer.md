---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c76bd152f64b337ca818c9e86b14fddbdaaf38cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455667"
---
# <span data-ttu-id="e1671-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e1671-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="e1671-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1671-102">SYNOPSIS</span></span>
<span data-ttu-id="e1671-103">取得 SCDPM 和 Azure 備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="e1671-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1671-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1671-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1671-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1671-105">DESCRIPTION</span></span>
<span data-ttu-id="e1671-106">**AzureRmRecoveryServicesBackupManagementServer** Cmdlet 會取得在電子倉庫中註冊的備份管理伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="e1671-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="e1671-107">備份管理伺服器有兩種類型：系統中心資料保護管理員 (SCDPM) 和 Azure 備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="e1671-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="e1671-108">備份管理伺服器會另行安裝，以管理備份業務流程。</span><span class="sxs-lookup"><span data-stu-id="e1671-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="e1671-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1671-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e1671-110">示例</span><span class="sxs-lookup"><span data-stu-id="e1671-110">EXAMPLES</span></span>

### <span data-ttu-id="e1671-111">範例1：取得所有備份管理伺服器</span><span class="sxs-lookup"><span data-stu-id="e1671-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="e1671-112">這個命令會取得所有使用保存庫註冊的備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="e1671-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="e1671-113">參數</span><span class="sxs-lookup"><span data-stu-id="e1671-113">PARAMETERS</span></span>

### <span data-ttu-id="e1671-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1671-114">-Name</span></span>
<span data-ttu-id="e1671-115">指定要取得之備份管理伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1671-115">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1671-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1671-116">-DefaultProfile</span></span>
<span data-ttu-id="e1671-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1671-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1671-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1671-118">CommonParameters</span></span>
<span data-ttu-id="e1671-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1671-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1671-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1671-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1671-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e1671-121">INPUTS</span></span>

## <span data-ttu-id="e1671-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e1671-122">OUTPUTS</span></span>

### <span data-ttu-id="e1671-123">BackupEngineBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="e1671-123">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="e1671-124">[System.object]. RecoveryServices [BackupEngineBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="e1671-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="e1671-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e1671-125">NOTES</span></span>

## <span data-ttu-id="e1671-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1671-126">RELATED LINKS</span></span>

[<span data-ttu-id="e1671-127">取消註冊-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e1671-127">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


