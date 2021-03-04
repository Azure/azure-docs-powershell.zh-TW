---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 50fb3af805adf4e42ab0b6bf1824b09473d98239
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911874"
---
# <span data-ttu-id="2f39d-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="2f39d-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="2f39d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f39d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f39d-103">獲得 SCDPM 和 Azure 備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="2f39d-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="2f39d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f39d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f39d-105">描述</span><span class="sxs-lookup"><span data-stu-id="2f39d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f39d-106">**Get-AzRecoveryServicesBackupManagementServer** Cmdlet 會取得在保存庫中註冊的備份管理伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="2f39d-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="2f39d-107">備份管理伺服器有兩種類型：System Center Data Protection Manager (SCDPM) Azure 備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="2f39d-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="2f39d-108">備份管理伺服器會個別安裝，以管理備份備份作業。</span><span class="sxs-lookup"><span data-stu-id="2f39d-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="2f39d-109">使用目前的 Cmdlet 之前，使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定庫內容。</span><span class="sxs-lookup"><span data-stu-id="2f39d-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2f39d-110">例子</span><span class="sxs-lookup"><span data-stu-id="2f39d-110">EXAMPLES</span></span>

### <span data-ttu-id="2f39d-111">範例 1：取得所有備份管理伺服器</span><span class="sxs-lookup"><span data-stu-id="2f39d-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="2f39d-112">此命令會向儲存庫登錄的所有備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="2f39d-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="2f39d-113">參數</span><span class="sxs-lookup"><span data-stu-id="2f39d-113">PARAMETERS</span></span>

### <span data-ttu-id="2f39d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f39d-114">-DefaultProfile</span></span>
<span data-ttu-id="2f39d-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f39d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f39d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f39d-116">-Name</span></span>
<span data-ttu-id="2f39d-117">指定要取得之備份管理伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f39d-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="2f39d-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2f39d-118">-VaultId</span></span>
<span data-ttu-id="2f39d-119">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f39d-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2f39d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f39d-120">CommonParameters</span></span>
<span data-ttu-id="2f39d-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f39d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f39d-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f39d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f39d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2f39d-123">INPUTS</span></span>

### <span data-ttu-id="2f39d-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2f39d-124">System.String</span></span>

## <span data-ttu-id="2f39d-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2f39d-125">OUTPUTS</span></span>

### <span data-ttu-id="2f39d-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="2f39d-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="2f39d-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2f39d-127">NOTES</span></span>

## <span data-ttu-id="2f39d-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f39d-128">RELATED LINKS</span></span>

[<span data-ttu-id="2f39d-129">未註冊-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="2f39d-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


