---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 4a083de76a3b3ebed0f2597f41cc500ddf084f9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915702"
---
# <span data-ttu-id="eacbe-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eacbe-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="eacbe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eacbe-102">SYNOPSIS</span></span>
<span data-ttu-id="eacbe-103">繼續 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="eacbe-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="eacbe-104">語法</span><span class="sxs-lookup"><span data-stu-id="eacbe-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eacbe-105">描述</span><span class="sxs-lookup"><span data-stu-id="eacbe-105">DESCRIPTION</span></span>
<span data-ttu-id="eacbe-106">此Resume-AzAnalysisServicesServer Cmdlet 會繼續 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="eacbe-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="eacbe-107">例子</span><span class="sxs-lookup"><span data-stu-id="eacbe-107">EXAMPLES</span></span>

### <span data-ttu-id="eacbe-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="eacbe-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="eacbe-109">此命令會繼續資源組測試組中名為 testerver 的暫停伺服器</span><span class="sxs-lookup"><span data-stu-id="eacbe-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="eacbe-110">參數</span><span class="sxs-lookup"><span data-stu-id="eacbe-110">PARAMETERS</span></span>

### <span data-ttu-id="eacbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eacbe-111">-DefaultProfile</span></span>
<span data-ttu-id="eacbe-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eacbe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eacbe-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="eacbe-113">-Name</span></span>
<span data-ttu-id="eacbe-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="eacbe-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="eacbe-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eacbe-115">-PassThru</span></span>
<span data-ttu-id="eacbe-116">如果作業順利完成，會返回已刪除的伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="eacbe-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="eacbe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eacbe-117">-ResourceGroupName</span></span>
<span data-ttu-id="eacbe-118">伺服器所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="eacbe-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="eacbe-119">-確認</span><span class="sxs-lookup"><span data-stu-id="eacbe-119">-Confirm</span></span>
<span data-ttu-id="eacbe-120">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="eacbe-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="eacbe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eacbe-121">-WhatIf</span></span>
<span data-ttu-id="eacbe-122">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="eacbe-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="eacbe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eacbe-123">CommonParameters</span></span>
<span data-ttu-id="eacbe-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eacbe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eacbe-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eacbe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eacbe-126">輸入</span><span class="sxs-lookup"><span data-stu-id="eacbe-126">INPUTS</span></span>

### <span data-ttu-id="eacbe-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eacbe-127">System.String</span></span>

## <span data-ttu-id="eacbe-128">輸出</span><span class="sxs-lookup"><span data-stu-id="eacbe-128">OUTPUTS</span></span>

### <span data-ttu-id="eacbe-129">Microsoft.Azure.Commands.AnalysisServices.models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eacbe-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="eacbe-130">筆記</span><span class="sxs-lookup"><span data-stu-id="eacbe-130">NOTES</span></span>
<span data-ttu-id="eacbe-131">別名：Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="eacbe-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="eacbe-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="eacbe-132">RELATED LINKS</span></span>

[<span data-ttu-id="eacbe-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eacbe-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="eacbe-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="eacbe-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
