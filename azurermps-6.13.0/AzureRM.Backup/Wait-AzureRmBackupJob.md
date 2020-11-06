---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: a5de80561ee0b80c2ce825db26e1de5c6f46b80b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447473"
---
# <span data-ttu-id="e0925-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="e0925-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="e0925-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0925-102">SYNOPSIS</span></span>
<span data-ttu-id="e0925-103">等待備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="e0925-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0925-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0925-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0925-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0925-105">DESCRIPTION</span></span>
<span data-ttu-id="e0925-106">**AzureRmBackupJob** Cmdlet 會等待 Azure 備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="e0925-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="e0925-107">備份作業可能需要花很長的時間。</span><span class="sxs-lookup"><span data-stu-id="e0925-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="e0925-108">如果您執行的是腳本的一部份備份作業，您可能會想要強制腳本在作業完成後再繼續其他工作。</span><span class="sxs-lookup"><span data-stu-id="e0925-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="e0925-109">包含此 Cmdlet 的腳本可能比輪詢備份服務的作業狀態更簡單。</span><span class="sxs-lookup"><span data-stu-id="e0925-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="e0925-110">示例</span><span class="sxs-lookup"><span data-stu-id="e0925-110">EXAMPLES</span></span>

## <span data-ttu-id="e0925-111">參數</span><span class="sxs-lookup"><span data-stu-id="e0925-111">PARAMETERS</span></span>

### <span data-ttu-id="e0925-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0925-112">-DefaultProfile</span></span>
<span data-ttu-id="e0925-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e0925-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0925-114">-工作</span><span class="sxs-lookup"><span data-stu-id="e0925-114">-Job</span></span>
<span data-ttu-id="e0925-115">指定此 Cmdlet 取消的作業。</span><span class="sxs-lookup"><span data-stu-id="e0925-115">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="e0925-116">若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0925-116">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0925-117">-超時</span><span class="sxs-lookup"><span data-stu-id="e0925-117">-TimeOut</span></span>
<span data-ttu-id="e0925-118">指定此 Cmdlet 等候作業完成所需的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e0925-118">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="e0925-119">我們建議您指定一個超時值。</span><span class="sxs-lookup"><span data-stu-id="e0925-119">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0925-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0925-120">CommonParameters</span></span>
<span data-ttu-id="e0925-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0925-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0925-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0925-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0925-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e0925-123">INPUTS</span></span>

### <span data-ttu-id="e0925-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e0925-124">System.Object</span></span>
<span data-ttu-id="e0925-125">參數：作業 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e0925-125">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="e0925-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e0925-126">OUTPUTS</span></span>

### <span data-ttu-id="e0925-127">AzureRMBackupJob 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="e0925-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="e0925-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e0925-128">NOTES</span></span>

## <span data-ttu-id="e0925-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0925-129">RELATED LINKS</span></span>

[<span data-ttu-id="e0925-130">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="e0925-130">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="e0925-131">停止 AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="e0925-131">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


