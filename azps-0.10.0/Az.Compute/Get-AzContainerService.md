---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796317"
---
# <span data-ttu-id="79c08-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="79c08-101">Get-AzContainerService</span></span>

## <span data-ttu-id="79c08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79c08-102">SYNOPSIS</span></span>
<span data-ttu-id="79c08-103">取得容器服務。</span><span class="sxs-lookup"><span data-stu-id="79c08-103">Gets a container service.</span></span>

## <span data-ttu-id="79c08-104">句法</span><span class="sxs-lookup"><span data-stu-id="79c08-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c08-105">說明</span><span class="sxs-lookup"><span data-stu-id="79c08-105">DESCRIPTION</span></span>
<span data-ttu-id="79c08-106">**AzContainerService** Cmdlet 會取得容器服務。</span><span class="sxs-lookup"><span data-stu-id="79c08-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="79c08-107">您可以查看容器服務的屬性，其中包括狀態、主版和代理程式的數目，以及主要和代理程式的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="79c08-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="79c08-108">示例</span><span class="sxs-lookup"><span data-stu-id="79c08-108">EXAMPLES</span></span>

### <span data-ttu-id="79c08-109">範例1：取得容器服務</span><span class="sxs-lookup"><span data-stu-id="79c08-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="79c08-110">這個命令會取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="79c08-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="79c08-111">參數</span><span class="sxs-lookup"><span data-stu-id="79c08-111">PARAMETERS</span></span>

### <span data-ttu-id="79c08-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c08-112">-DefaultProfile</span></span>
<span data-ttu-id="79c08-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79c08-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c08-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="79c08-114">-Name</span></span>
<span data-ttu-id="79c08-115">指定此 Cmdlet 所取得之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="79c08-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="79c08-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c08-116">-ResourceGroupName</span></span>
<span data-ttu-id="79c08-117">指定此 Cmdlet 所取得之容器服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="79c08-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="79c08-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c08-118">CommonParameters</span></span>
<span data-ttu-id="79c08-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79c08-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c08-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79c08-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c08-121">輸入</span><span class="sxs-lookup"><span data-stu-id="79c08-121">INPUTS</span></span>

### <span data-ttu-id="79c08-122">所有</span><span class="sxs-lookup"><span data-stu-id="79c08-122">None</span></span>
<span data-ttu-id="79c08-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="79c08-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79c08-124">輸出</span><span class="sxs-lookup"><span data-stu-id="79c08-124">OUTPUTS</span></span>

### <span data-ttu-id="79c08-125">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="79c08-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="79c08-126">筆記</span><span class="sxs-lookup"><span data-stu-id="79c08-126">NOTES</span></span>

## <span data-ttu-id="79c08-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="79c08-127">RELATED LINKS</span></span>

[<span data-ttu-id="79c08-128">新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="79c08-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="79c08-129">移除-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="79c08-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="79c08-130">更新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="79c08-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


