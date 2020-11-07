---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625108"
---
# <span data-ttu-id="1192b-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1192b-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="1192b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1192b-102">SYNOPSIS</span></span>
<span data-ttu-id="1192b-103">從保存庫登出 Windows Server 或其他容器。</span><span class="sxs-lookup"><span data-stu-id="1192b-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1192b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1192b-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1192b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1192b-105">DESCRIPTION</span></span>
<span data-ttu-id="1192b-106">[ **登出 AzureRmRecoveryServicesBackupContainer** ] Cmdlet 會從保存庫中登出 Windows Server 或其他備份容器。</span><span class="sxs-lookup"><span data-stu-id="1192b-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="1192b-107">這個 Cmdlet 會從保存庫移除容器的參照。</span><span class="sxs-lookup"><span data-stu-id="1192b-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="1192b-108">在您可以取消註冊容器之前，您必須刪除所有與該容器相關聯的受保護資料。</span><span class="sxs-lookup"><span data-stu-id="1192b-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="1192b-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1192b-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1192b-110">示例</span><span class="sxs-lookup"><span data-stu-id="1192b-110">EXAMPLES</span></span>

### <span data-ttu-id="1192b-111">範例1：從保存庫登出 Windows Server</span><span class="sxs-lookup"><span data-stu-id="1192b-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="1192b-112">第一個命令會取得名為 server01.contoso.com 的 Windows 容器，該容器已在 vault 中註冊，然後將其儲存在 $Cont 變數中。</span><span class="sxs-lookup"><span data-stu-id="1192b-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="1192b-113">第二個命令會從 Azure 備份電子倉庫登出指定的 Windows 伺服器。</span><span class="sxs-lookup"><span data-stu-id="1192b-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="1192b-114">參數</span><span class="sxs-lookup"><span data-stu-id="1192b-114">PARAMETERS</span></span>

### <span data-ttu-id="1192b-115">-容器</span><span class="sxs-lookup"><span data-stu-id="1192b-115">-Container</span></span>
<span data-ttu-id="1192b-116">指定要取消註冊的備份容器物件。</span><span class="sxs-lookup"><span data-stu-id="1192b-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="1192b-117">若要取得 **BackupContainer** 物件，請使用 Get-AzureRmRecoveryServicesBackupContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1192b-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1192b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1192b-118">-DefaultProfile</span></span>
<span data-ttu-id="1192b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1192b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1192b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1192b-120">CommonParameters</span></span>
<span data-ttu-id="1192b-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1192b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1192b-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1192b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1192b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="1192b-123">INPUTS</span></span>

## <span data-ttu-id="1192b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1192b-124">OUTPUTS</span></span>

## <span data-ttu-id="1192b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1192b-125">NOTES</span></span>

## <span data-ttu-id="1192b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1192b-126">RELATED LINKS</span></span>

[<span data-ttu-id="1192b-127">AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1192b-127">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


