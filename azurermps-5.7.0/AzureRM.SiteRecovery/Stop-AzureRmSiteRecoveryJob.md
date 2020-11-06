---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/stop-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 44875207b5a4317b2ceb9a0284a3818a6be36298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444315"
---
# <span data-ttu-id="5843c-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5843c-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="5843c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5843c-102">SYNOPSIS</span></span>
<span data-ttu-id="5843c-103">停止網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="5843c-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5843c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5843c-104">SYNTAX</span></span>

### <span data-ttu-id="5843c-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5843c-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5843c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5843c-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5843c-107">說明</span><span class="sxs-lookup"><span data-stu-id="5843c-107">DESCRIPTION</span></span>
<span data-ttu-id="5843c-108">**AzureRmSiteRecoveryJob** Cmdlet 會停止 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="5843c-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="5843c-109">示例</span><span class="sxs-lookup"><span data-stu-id="5843c-109">EXAMPLES</span></span>

## <span data-ttu-id="5843c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5843c-110">PARAMETERS</span></span>

### <span data-ttu-id="5843c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5843c-111">-DefaultProfile</span></span>
<span data-ttu-id="5843c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5843c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5843c-113">-工作</span><span class="sxs-lookup"><span data-stu-id="5843c-113">-Job</span></span>
<span data-ttu-id="5843c-114">指定要停止的 Site Recovery 工作物件。</span><span class="sxs-lookup"><span data-stu-id="5843c-114">Specifies the Site Recovery job object to stop.</span></span>

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

### <span data-ttu-id="5843c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5843c-115">-Name</span></span>
<span data-ttu-id="5843c-116">指定要停止的網站恢復作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="5843c-116">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="5843c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5843c-117">CommonParameters</span></span>
<span data-ttu-id="5843c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5843c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5843c-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5843c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5843c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5843c-120">INPUTS</span></span>

### <span data-ttu-id="5843c-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="5843c-121">ASRJob</span></span>
<span data-ttu-id="5843c-122">參數「作業」接受管道中類型 ' ASRJob」的值</span><span class="sxs-lookup"><span data-stu-id="5843c-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="5843c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5843c-123">OUTPUTS</span></span>

### <span data-ttu-id="5843c-124">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5843c-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5843c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5843c-125">NOTES</span></span>

## <span data-ttu-id="5843c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5843c-126">RELATED LINKS</span></span>

[<span data-ttu-id="5843c-127">AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5843c-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5843c-128">重新開機-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5843c-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5843c-129">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5843c-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
