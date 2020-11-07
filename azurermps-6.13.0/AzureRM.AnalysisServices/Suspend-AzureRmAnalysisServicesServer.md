---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0fc666ef1b747c7c114de560d241bcc2ac7be1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624963"
---
# <span data-ttu-id="38ffc-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="38ffc-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="38ffc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="38ffc-103">暫停分析服務伺服器實例</span><span class="sxs-lookup"><span data-stu-id="38ffc-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38ffc-104">句法</span><span class="sxs-lookup"><span data-stu-id="38ffc-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ffc-105">說明</span><span class="sxs-lookup"><span data-stu-id="38ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="38ffc-106">Suspend-AzureRmAnalysisServicesServer Cmdlet 會暫停 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="38ffc-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="38ffc-107">示例</span><span class="sxs-lookup"><span data-stu-id="38ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="38ffc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="38ffc-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="38ffc-109">這個命令會在 resourcegroup testgroup 中暫停名為 testserver 的活動伺服器</span><span class="sxs-lookup"><span data-stu-id="38ffc-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="38ffc-110">參數</span><span class="sxs-lookup"><span data-stu-id="38ffc-110">PARAMETERS</span></span>

### <span data-ttu-id="38ffc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ffc-111">-DefaultProfile</span></span>
<span data-ttu-id="38ffc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38ffc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38ffc-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="38ffc-113">-Name</span></span>
<span data-ttu-id="38ffc-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="38ffc-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="38ffc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38ffc-115">-PassThru</span></span>
<span data-ttu-id="38ffc-116">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="38ffc-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="38ffc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ffc-117">-ResourceGroupName</span></span>
<span data-ttu-id="38ffc-118">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="38ffc-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="38ffc-119">-確認</span><span class="sxs-lookup"><span data-stu-id="38ffc-119">-Confirm</span></span>
<span data-ttu-id="38ffc-120">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="38ffc-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="38ffc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ffc-121">-WhatIf</span></span>
<span data-ttu-id="38ffc-122">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="38ffc-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="38ffc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ffc-123">CommonParameters</span></span>
<span data-ttu-id="38ffc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38ffc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ffc-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38ffc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ffc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="38ffc-126">INPUTS</span></span>

### <span data-ttu-id="38ffc-127">System.object</span><span class="sxs-lookup"><span data-stu-id="38ffc-127">System.String</span></span>

## <span data-ttu-id="38ffc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="38ffc-128">OUTPUTS</span></span>

### <span data-ttu-id="38ffc-129">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="38ffc-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="38ffc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="38ffc-130">NOTES</span></span>
<span data-ttu-id="38ffc-131">別名： Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="38ffc-131">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="38ffc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="38ffc-132">RELATED LINKS</span></span>

[<span data-ttu-id="38ffc-133">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="38ffc-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="38ffc-134">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="38ffc-134">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

