---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 782fcae5d243a1686e20237843d69b02564755f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916305"
---
# <span data-ttu-id="17ffd-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="17ffd-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="17ffd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="17ffd-103">刪除 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="17ffd-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="17ffd-104">語法</span><span class="sxs-lookup"><span data-stu-id="17ffd-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17ffd-105">描述</span><span class="sxs-lookup"><span data-stu-id="17ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="17ffd-106">此Remove-AzAnalysisServicesServer Cmdlet 會刪除 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="17ffd-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="17ffd-107">例子</span><span class="sxs-lookup"><span data-stu-id="17ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="17ffd-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="17ffd-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="17ffd-109">此命令會移除資源組測試組中名為 testerver 的伺服器</span><span class="sxs-lookup"><span data-stu-id="17ffd-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="17ffd-110">參數</span><span class="sxs-lookup"><span data-stu-id="17ffd-110">PARAMETERS</span></span>

### <span data-ttu-id="17ffd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ffd-111">-DefaultProfile</span></span>
<span data-ttu-id="17ffd-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="17ffd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17ffd-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="17ffd-113">-Name</span></span>
<span data-ttu-id="17ffd-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="17ffd-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="17ffd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17ffd-115">-PassThru</span></span>
<span data-ttu-id="17ffd-116">如果作業順利完成，會返回已刪除的伺服器詳細資料</span><span class="sxs-lookup"><span data-stu-id="17ffd-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="17ffd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ffd-117">-ResourceGroupName</span></span>
<span data-ttu-id="17ffd-118">伺服器所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="17ffd-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="17ffd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="17ffd-119">-Confirm</span></span>
<span data-ttu-id="17ffd-120">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="17ffd-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="17ffd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17ffd-121">-WhatIf</span></span>
<span data-ttu-id="17ffd-122">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="17ffd-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="17ffd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ffd-123">CommonParameters</span></span>
<span data-ttu-id="17ffd-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17ffd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ffd-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="17ffd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ffd-126">輸入</span><span class="sxs-lookup"><span data-stu-id="17ffd-126">INPUTS</span></span>

### <span data-ttu-id="17ffd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="17ffd-127">System.String</span></span>

## <span data-ttu-id="17ffd-128">輸出</span><span class="sxs-lookup"><span data-stu-id="17ffd-128">OUTPUTS</span></span>

### <span data-ttu-id="17ffd-129">Microsoft.Azure.Commands.AnalysisServices.models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="17ffd-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="17ffd-130">筆記</span><span class="sxs-lookup"><span data-stu-id="17ffd-130">NOTES</span></span>
<span data-ttu-id="17ffd-131">別名：Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="17ffd-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="17ffd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="17ffd-132">RELATED LINKS</span></span>

[<span data-ttu-id="17ffd-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="17ffd-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="17ffd-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="17ffd-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
