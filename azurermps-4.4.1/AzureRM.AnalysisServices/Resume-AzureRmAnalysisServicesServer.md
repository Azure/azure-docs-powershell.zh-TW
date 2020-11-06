---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445247"
---
# <span data-ttu-id="e04fd-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e04fd-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="e04fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e04fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e04fd-103">繼續分析服務伺服器實例</span><span class="sxs-lookup"><span data-stu-id="e04fd-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e04fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="e04fd-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e04fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="e04fd-105">DESCRIPTION</span></span>
<span data-ttu-id="e04fd-106">Resume-AzureRmAnalysisServicesServer Cmdlet 會繼續執行 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="e04fd-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="e04fd-107">示例</span><span class="sxs-lookup"><span data-stu-id="e04fd-107">EXAMPLES</span></span>

### <span data-ttu-id="e04fd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e04fd-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="e04fd-109">這個命令會在 resourcegroup testgroup 中繼續已暫停的伺服器（名為 testserver）</span><span class="sxs-lookup"><span data-stu-id="e04fd-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="e04fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="e04fd-110">PARAMETERS</span></span>

### <span data-ttu-id="e04fd-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="e04fd-111">-Name</span></span>
<span data-ttu-id="e04fd-112">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="e04fd-112">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e04fd-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e04fd-113">-PassThru</span></span>
<span data-ttu-id="e04fd-114">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="e04fd-114">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e04fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="e04fd-116">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e04fd-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="e04fd-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e04fd-117">-Confirm</span></span>
<span data-ttu-id="e04fd-118">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="e04fd-118">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04fd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04fd-119">-WhatIf</span></span>
<span data-ttu-id="e04fd-120">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="e04fd-120">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04fd-121">CommonParameters</span></span>
<span data-ttu-id="e04fd-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e04fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04fd-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e04fd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04fd-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e04fd-124">INPUTS</span></span>

## <span data-ttu-id="e04fd-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e04fd-125">OUTPUTS</span></span>

### <span data-ttu-id="e04fd-126">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="e04fd-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="e04fd-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e04fd-127">NOTES</span></span>
<span data-ttu-id="e04fd-128">別名： Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="e04fd-128">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="e04fd-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e04fd-129">RELATED LINKS</span></span>

[<span data-ttu-id="e04fd-130">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e04fd-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="e04fd-131">暫停-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e04fd-131">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
