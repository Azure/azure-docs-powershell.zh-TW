---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 6ae660eae9e597d92e162529ff244431d4720418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447489"
---
# <span data-ttu-id="50e14-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="50e14-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="50e14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50e14-102">SYNOPSIS</span></span>
<span data-ttu-id="50e14-103">Reregisters 要連線至備份保存庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="50e14-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50e14-104">句法</span><span class="sxs-lookup"><span data-stu-id="50e14-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e14-105">說明</span><span class="sxs-lookup"><span data-stu-id="50e14-105">DESCRIPTION</span></span>
<span data-ttu-id="50e14-106">**Enable-AzureRmBackupContainerReregistration** Cmdlet 會 reregisters 伺服器以連線至 Azure 備份電子倉庫，並繼續備份復原點鏈。</span><span class="sxs-lookup"><span data-stu-id="50e14-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>
<span data-ttu-id="50e14-107">如果您銷毀伺服器，其所有雲端備份點都會保留在備份保存庫中。</span><span class="sxs-lookup"><span data-stu-id="50e14-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="50e14-108">如果您建立替換伺服器並指派相同的完整功能變數名稱，您可以將伺服器連線到相同的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="50e14-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="50e14-109">這個 Cmdlet 可讓備份進行備份，並將新的備份點新增到現有集合。</span><span class="sxs-lookup"><span data-stu-id="50e14-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="50e14-110">新的伺服器會在備份鏈中繼續。</span><span class="sxs-lookup"><span data-stu-id="50e14-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="50e14-111">示例</span><span class="sxs-lookup"><span data-stu-id="50e14-111">EXAMPLES</span></span>

## <span data-ttu-id="50e14-112">參數</span><span class="sxs-lookup"><span data-stu-id="50e14-112">PARAMETERS</span></span>

### <span data-ttu-id="50e14-113">-容器</span><span class="sxs-lookup"><span data-stu-id="50e14-113">-Container</span></span>
<span data-ttu-id="50e14-114">指定此 Cmdlet reregisters 的容器。</span><span class="sxs-lookup"><span data-stu-id="50e14-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="50e14-115">若要取得 **AzureRmBackupContainer** ，請使用 Get-AzureRmBackupContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50e14-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50e14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e14-116">-DefaultProfile</span></span>
<span data-ttu-id="50e14-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="50e14-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50e14-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e14-118">CommonParameters</span></span>
<span data-ttu-id="50e14-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50e14-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e14-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50e14-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e14-121">輸入</span><span class="sxs-lookup"><span data-stu-id="50e14-121">INPUTS</span></span>

### <span data-ttu-id="50e14-122">AzureRMBackupContainer 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="50e14-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="50e14-123">參數：容器 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="50e14-123">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="50e14-124">輸出</span><span class="sxs-lookup"><span data-stu-id="50e14-124">OUTPUTS</span></span>

### <span data-ttu-id="50e14-125">System.void</span><span class="sxs-lookup"><span data-stu-id="50e14-125">System.Void</span></span>

## <span data-ttu-id="50e14-126">筆記</span><span class="sxs-lookup"><span data-stu-id="50e14-126">NOTES</span></span>

## <span data-ttu-id="50e14-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="50e14-127">RELATED LINKS</span></span>

[<span data-ttu-id="50e14-128">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="50e14-128">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="50e14-129">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="50e14-129">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


