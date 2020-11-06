---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/resume-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: aae0bf7c2ec4a166d48edb032d6c21918dc3ae6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448554"
---
# <span data-ttu-id="5c88e-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c88e-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="5c88e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c88e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c88e-103">繼續暫停的網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="5c88e-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c88e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c88e-104">SYNTAX</span></span>

### <span data-ttu-id="5c88e-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5c88e-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c88e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5c88e-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c88e-107">說明</span><span class="sxs-lookup"><span data-stu-id="5c88e-107">DESCRIPTION</span></span>
<span data-ttu-id="5c88e-108">**Resume AzureRmSiteRecoveryJob** Cmdlet 會繼續執行暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="5c88e-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="5c88e-109">示例</span><span class="sxs-lookup"><span data-stu-id="5c88e-109">EXAMPLES</span></span>

## <span data-ttu-id="5c88e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5c88e-110">PARAMETERS</span></span>

### <span data-ttu-id="5c88e-111">-批註</span><span class="sxs-lookup"><span data-stu-id="5c88e-111">-Comments</span></span>
<span data-ttu-id="5c88e-112">指定作業記錄的批註。</span><span class="sxs-lookup"><span data-stu-id="5c88e-112">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c88e-113">-DefaultProfile</span></span>
<span data-ttu-id="5c88e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c88e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c88e-115">-工作</span><span class="sxs-lookup"><span data-stu-id="5c88e-115">-Job</span></span>
<span data-ttu-id="5c88e-116">指定 Site Recovery 工作物件。</span><span class="sxs-lookup"><span data-stu-id="5c88e-116">Specifies the Site Recovery job object.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c88e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c88e-117">-Name</span></span>
<span data-ttu-id="5c88e-118">指定作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="5c88e-118">Specifies the unique name for the job.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c88e-119">CommonParameters</span></span>
<span data-ttu-id="5c88e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c88e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c88e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c88e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c88e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="5c88e-122">INPUTS</span></span>

### <span data-ttu-id="5c88e-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c88e-123">ASRJob</span></span>
<span data-ttu-id="5c88e-124">參數「作業」接受管道中類型 ' ASRJob」的值</span><span class="sxs-lookup"><span data-stu-id="5c88e-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="5c88e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="5c88e-125">OUTPUTS</span></span>

### <span data-ttu-id="5c88e-126">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5c88e-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c88e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5c88e-127">NOTES</span></span>

## <span data-ttu-id="5c88e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c88e-128">RELATED LINKS</span></span>

[<span data-ttu-id="5c88e-129">AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c88e-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5c88e-130">重新開機-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c88e-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5c88e-131">停止 AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c88e-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
