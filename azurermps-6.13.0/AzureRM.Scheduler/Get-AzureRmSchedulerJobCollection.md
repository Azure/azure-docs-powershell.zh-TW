---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 402bb79dbd3b767cbc285600b9c81e27f244141e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455020"
---
# <span data-ttu-id="1b2c2-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1b2c2-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="1b2c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2c2-103">取得作業集合。</span><span class="sxs-lookup"><span data-stu-id="1b2c2-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b2c2-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b2c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2c2-106">**AzureRmSchedulerJobCollection** Cmdlet 會取得 Azure 排程器中的作業集合。</span><span class="sxs-lookup"><span data-stu-id="1b2c2-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="1b2c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b2c2-107">EXAMPLES</span></span>

## <span data-ttu-id="1b2c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="1b2c2-108">PARAMETERS</span></span>

### <span data-ttu-id="1b2c2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2c2-109">-DefaultProfile</span></span>
<span data-ttu-id="1b2c2-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b2c2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2c2-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1b2c2-111">-JobCollectionName</span></span>
<span data-ttu-id="1b2c2-112">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b2c2-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2c2-113">-ResourceGroupName</span></span>
<span data-ttu-id="1b2c2-114">指定此 Cmdlet 取得作業集合的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1b2c2-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2c2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2c2-115">CommonParameters</span></span>
<span data-ttu-id="1b2c2-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b2c2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2c2-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b2c2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2c2-118">輸入</span><span class="sxs-lookup"><span data-stu-id="1b2c2-118">INPUTS</span></span>

### <span data-ttu-id="1b2c2-119">System.object</span><span class="sxs-lookup"><span data-stu-id="1b2c2-119">System.String</span></span>

## <span data-ttu-id="1b2c2-120">輸出</span><span class="sxs-lookup"><span data-stu-id="1b2c2-120">OUTPUTS</span></span>

### <span data-ttu-id="1b2c2-121">PSJobCollectionDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b2c2-121">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="1b2c2-122">筆記</span><span class="sxs-lookup"><span data-stu-id="1b2c2-122">NOTES</span></span>

## <span data-ttu-id="1b2c2-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b2c2-123">RELATED LINKS</span></span>

[<span data-ttu-id="1b2c2-124">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1b2c2-124">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1b2c2-125">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1b2c2-125">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1b2c2-126">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1b2c2-126">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1b2c2-127">移除-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1b2c2-127">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1b2c2-128">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1b2c2-128">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


