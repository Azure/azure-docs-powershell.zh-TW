---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: ecd9e83607da048246ec996188fd9a31d231ff32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614093"
---
# <span data-ttu-id="d43ff-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d43ff-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d43ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d43ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d43ff-103">暫停分析服務伺服器實例</span><span class="sxs-lookup"><span data-stu-id="d43ff-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="d43ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="d43ff-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d43ff-105">說明</span><span class="sxs-lookup"><span data-stu-id="d43ff-105">DESCRIPTION</span></span>
<span data-ttu-id="d43ff-106">Suspend-AzAnalysisServicesServer Cmdlet 會暫停 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="d43ff-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="d43ff-107">示例</span><span class="sxs-lookup"><span data-stu-id="d43ff-107">EXAMPLES</span></span>

### <span data-ttu-id="d43ff-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d43ff-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="d43ff-109">這個命令會在 resourcegroup testgroup 中暫停名為 testserver 的活動伺服器</span><span class="sxs-lookup"><span data-stu-id="d43ff-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d43ff-110">參數</span><span class="sxs-lookup"><span data-stu-id="d43ff-110">PARAMETERS</span></span>

### <span data-ttu-id="d43ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43ff-111">-DefaultProfile</span></span>
<span data-ttu-id="d43ff-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d43ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ff-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d43ff-113">-Name</span></span>
<span data-ttu-id="d43ff-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="d43ff-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43ff-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d43ff-115">-PassThru</span></span>
<span data-ttu-id="d43ff-116">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="d43ff-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="d43ff-118">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d43ff-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43ff-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d43ff-119">-Confirm</span></span>
<span data-ttu-id="d43ff-120">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="d43ff-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43ff-121">-WhatIf</span></span>
<span data-ttu-id="d43ff-122">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="d43ff-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43ff-123">CommonParameters</span></span>
<span data-ttu-id="d43ff-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d43ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43ff-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d43ff-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43ff-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d43ff-126">INPUTS</span></span>

### <span data-ttu-id="d43ff-127">System.object</span><span class="sxs-lookup"><span data-stu-id="d43ff-127">System.String</span></span>

## <span data-ttu-id="d43ff-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d43ff-128">OUTPUTS</span></span>

### <span data-ttu-id="d43ff-129">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="d43ff-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d43ff-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d43ff-130">NOTES</span></span>
<span data-ttu-id="d43ff-131">別名： Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="d43ff-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="d43ff-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d43ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="d43ff-133">AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d43ff-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d43ff-134">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d43ff-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

