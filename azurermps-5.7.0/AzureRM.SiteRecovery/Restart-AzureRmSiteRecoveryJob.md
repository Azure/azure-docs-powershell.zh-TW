---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444320"
---
# <span data-ttu-id="82259-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="82259-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="82259-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82259-102">SYNOPSIS</span></span>
<span data-ttu-id="82259-103">重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="82259-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82259-104">句法</span><span class="sxs-lookup"><span data-stu-id="82259-104">SYNTAX</span></span>

### <span data-ttu-id="82259-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="82259-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82259-106">ByName</span><span class="sxs-lookup"><span data-stu-id="82259-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82259-107">說明</span><span class="sxs-lookup"><span data-stu-id="82259-107">DESCRIPTION</span></span>
<span data-ttu-id="82259-108">**Restart AzureRmSiteRecoveryJob** Cmdlet 會重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="82259-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="82259-109">示例</span><span class="sxs-lookup"><span data-stu-id="82259-109">EXAMPLES</span></span>

## <span data-ttu-id="82259-110">參數</span><span class="sxs-lookup"><span data-stu-id="82259-110">PARAMETERS</span></span>

### <span data-ttu-id="82259-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82259-111">-DefaultProfile</span></span>
<span data-ttu-id="82259-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82259-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82259-113">-工作</span><span class="sxs-lookup"><span data-stu-id="82259-113">-Job</span></span>
<span data-ttu-id="82259-114">指定 Site Recovery 工作物件。</span><span class="sxs-lookup"><span data-stu-id="82259-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="82259-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="82259-115">-Name</span></span>
<span data-ttu-id="82259-116">指定作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="82259-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="82259-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82259-117">CommonParameters</span></span>
<span data-ttu-id="82259-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82259-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82259-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82259-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82259-120">輸入</span><span class="sxs-lookup"><span data-stu-id="82259-120">INPUTS</span></span>

### <span data-ttu-id="82259-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="82259-121">ASRJob</span></span>
<span data-ttu-id="82259-122">參數「作業」接受管道中類型 ' ASRJob」的值</span><span class="sxs-lookup"><span data-stu-id="82259-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="82259-123">輸出</span><span class="sxs-lookup"><span data-stu-id="82259-123">OUTPUTS</span></span>

### <span data-ttu-id="82259-124">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="82259-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="82259-125">筆記</span><span class="sxs-lookup"><span data-stu-id="82259-125">NOTES</span></span>

## <span data-ttu-id="82259-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="82259-126">RELATED LINKS</span></span>

[<span data-ttu-id="82259-127">AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="82259-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="82259-128">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="82259-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="82259-129">停止 AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="82259-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
