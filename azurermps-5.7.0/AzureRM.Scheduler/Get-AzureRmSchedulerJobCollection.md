---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625441"
---
# <span data-ttu-id="ba926-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ba926-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="ba926-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba926-102">SYNOPSIS</span></span>
<span data-ttu-id="ba926-103">取得作業集合。</span><span class="sxs-lookup"><span data-stu-id="ba926-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba926-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba926-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba926-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba926-105">DESCRIPTION</span></span>
<span data-ttu-id="ba926-106">**AzureRmSchedulerJobCollection** Cmdlet 會取得 Azure 排程器中的作業集合。</span><span class="sxs-lookup"><span data-stu-id="ba926-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="ba926-107">示例</span><span class="sxs-lookup"><span data-stu-id="ba926-107">EXAMPLES</span></span>

## <span data-ttu-id="ba926-108">參數</span><span class="sxs-lookup"><span data-stu-id="ba926-108">PARAMETERS</span></span>

### <span data-ttu-id="ba926-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba926-109">-DefaultProfile</span></span>
<span data-ttu-id="ba926-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba926-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba926-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ba926-111">-JobCollectionName</span></span>
<span data-ttu-id="ba926-112">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba926-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba926-113">-ResourceGroupName</span></span>
<span data-ttu-id="ba926-114">指定此 Cmdlet 取得作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ba926-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba926-115">CommonParameters</span></span>
<span data-ttu-id="ba926-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba926-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba926-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba926-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba926-118">輸入</span><span class="sxs-lookup"><span data-stu-id="ba926-118">INPUTS</span></span>

### <span data-ttu-id="ba926-119">所有</span><span class="sxs-lookup"><span data-stu-id="ba926-119">None</span></span>
<span data-ttu-id="ba926-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ba926-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba926-121">輸出</span><span class="sxs-lookup"><span data-stu-id="ba926-121">OUTPUTS</span></span>

### <span data-ttu-id="ba926-122">System.object</span><span class="sxs-lookup"><span data-stu-id="ba926-122">System.Object</span></span>

## <span data-ttu-id="ba926-123">筆記</span><span class="sxs-lookup"><span data-stu-id="ba926-123">NOTES</span></span>

## <span data-ttu-id="ba926-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba926-124">RELATED LINKS</span></span>

[<span data-ttu-id="ba926-125">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ba926-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ba926-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ba926-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ba926-127">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ba926-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ba926-128">移除-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ba926-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ba926-129">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ba926-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


