---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 116dfd9d38325682e6a80361b40bc8dd84b133fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447102"
---
# <span data-ttu-id="881a0-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="881a0-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="881a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="881a0-102">SYNOPSIS</span></span>
<span data-ttu-id="881a0-103">暫停分析服務伺服器實例</span><span class="sxs-lookup"><span data-stu-id="881a0-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="881a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="881a0-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="881a0-105">說明</span><span class="sxs-lookup"><span data-stu-id="881a0-105">DESCRIPTION</span></span>
<span data-ttu-id="881a0-106">Suspend-AzureRmAnalysisServicesServer Cmdlet 會暫停 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="881a0-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="881a0-107">示例</span><span class="sxs-lookup"><span data-stu-id="881a0-107">EXAMPLES</span></span>

### <span data-ttu-id="881a0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="881a0-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="881a0-109">這個命令會在 resourcegroup testgroup 中暫停名為 testserver 的活動伺服器</span><span class="sxs-lookup"><span data-stu-id="881a0-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="881a0-110">參數</span><span class="sxs-lookup"><span data-stu-id="881a0-110">PARAMETERS</span></span>

### <span data-ttu-id="881a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="881a0-111">-DefaultProfile</span></span>
<span data-ttu-id="881a0-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="881a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="881a0-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="881a0-113">-Name</span></span>
<span data-ttu-id="881a0-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="881a0-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="881a0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="881a0-115">-PassThru</span></span>
<span data-ttu-id="881a0-116">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="881a0-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="881a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="881a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="881a0-118">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="881a0-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="881a0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="881a0-119">-Confirm</span></span>
<span data-ttu-id="881a0-120">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="881a0-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="881a0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="881a0-121">-WhatIf</span></span>
<span data-ttu-id="881a0-122">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="881a0-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="881a0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="881a0-123">CommonParameters</span></span>
<span data-ttu-id="881a0-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="881a0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="881a0-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="881a0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="881a0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="881a0-126">INPUTS</span></span>

### <span data-ttu-id="881a0-127">所有</span><span class="sxs-lookup"><span data-stu-id="881a0-127">None</span></span>
<span data-ttu-id="881a0-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="881a0-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="881a0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="881a0-129">OUTPUTS</span></span>

### <span data-ttu-id="881a0-130">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="881a0-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="881a0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="881a0-131">NOTES</span></span>
<span data-ttu-id="881a0-132">別名： Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="881a0-132">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="881a0-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="881a0-133">RELATED LINKS</span></span>

[<span data-ttu-id="881a0-134">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="881a0-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="881a0-135">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="881a0-135">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

