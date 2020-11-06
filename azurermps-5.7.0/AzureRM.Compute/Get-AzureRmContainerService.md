---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449950"
---
# <span data-ttu-id="bd1dc-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bd1dc-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="bd1dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="bd1dc-103">取得容器服務。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd1dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd1dc-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="bd1dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="bd1dc-106">**AzureRmContainerService** Cmdlet 會取得容器服務。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="bd1dc-107">您可以查看容器服務的屬性，其中包括狀態、主版和代理程式的數目，以及主要和代理程式的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="bd1dc-108">示例</span><span class="sxs-lookup"><span data-stu-id="bd1dc-108">EXAMPLES</span></span>

### <span data-ttu-id="bd1dc-109">範例1：取得容器服務</span><span class="sxs-lookup"><span data-stu-id="bd1dc-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="bd1dc-110">這個命令會取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="bd1dc-111">參數</span><span class="sxs-lookup"><span data-stu-id="bd1dc-111">PARAMETERS</span></span>

### <span data-ttu-id="bd1dc-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd1dc-112">-Name</span></span>
<span data-ttu-id="bd1dc-113">指定此 Cmdlet 所取得之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1dc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd1dc-114">-ResourceGroupName</span></span>
<span data-ttu-id="bd1dc-115">指定此 Cmdlet 所取得之容器服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1dc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd1dc-116">CommonParameters</span></span>
<span data-ttu-id="bd1dc-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd1dc-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd1dc-119">輸入</span><span class="sxs-lookup"><span data-stu-id="bd1dc-119">INPUTS</span></span>

### <span data-ttu-id="bd1dc-120">所有</span><span class="sxs-lookup"><span data-stu-id="bd1dc-120">None</span></span>
<span data-ttu-id="bd1dc-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bd1dc-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd1dc-122">輸出</span><span class="sxs-lookup"><span data-stu-id="bd1dc-122">OUTPUTS</span></span>

## <span data-ttu-id="bd1dc-123">筆記</span><span class="sxs-lookup"><span data-stu-id="bd1dc-123">NOTES</span></span>

## <span data-ttu-id="bd1dc-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd1dc-124">RELATED LINKS</span></span>

[<span data-ttu-id="bd1dc-125">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bd1dc-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="bd1dc-126">移除-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bd1dc-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="bd1dc-127">更新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bd1dc-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


