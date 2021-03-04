---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: 85d391e3f50bb06ddbc5ec8937b643d9dcbce492
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903801"
---
# <span data-ttu-id="0ed44-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0ed44-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="0ed44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0ed44-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed44-103">移除資源的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="0ed44-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="0ed44-104">語法</span><span class="sxs-lookup"><span data-stu-id="0ed44-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ed44-105">描述</span><span class="sxs-lookup"><span data-stu-id="0ed44-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed44-106">**Remove-AzDiagnosticSetting** Cmdlet 會移除特定資源的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="0ed44-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="0ed44-107">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="0ed44-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0ed44-108">例子</span><span class="sxs-lookup"><span data-stu-id="0ed44-108">EXAMPLES</span></span>

### <span data-ttu-id="0ed44-109">範例 1：移除資源 (服務) 診斷設定</span><span class="sxs-lookup"><span data-stu-id="0ed44-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="0ed44-110">此命令會移除資源名稱為 Resource01 (服務) 的預設診斷設定。</span><span class="sxs-lookup"><span data-stu-id="0ed44-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="0ed44-111">範例 2：移除資源指定名稱識別的預設診斷設定</span><span class="sxs-lookup"><span data-stu-id="0ed44-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="0ed44-112">此命令會移除名為 Resource01 之資源的名為 myDiagSetting 的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="0ed44-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="0ed44-113">參數</span><span class="sxs-lookup"><span data-stu-id="0ed44-113">PARAMETERS</span></span>

### <span data-ttu-id="0ed44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed44-114">-DefaultProfile</span></span>
<span data-ttu-id="0ed44-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ed44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed44-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ed44-116">-Name</span></span>
<span data-ttu-id="0ed44-117">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ed44-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="0ed44-118">如果沒有將通話預設為「服務」，則此 Cmdlet 只會停用所有計量/記錄類別。</span><span class="sxs-lookup"><span data-stu-id="0ed44-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="0ed44-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ed44-119">-ResourceId</span></span>
<span data-ttu-id="0ed44-120">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ed44-120">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed44-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0ed44-121">-Confirm</span></span>
<span data-ttu-id="0ed44-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0ed44-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed44-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed44-123">-WhatIf</span></span>
<span data-ttu-id="0ed44-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ed44-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ed44-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ed44-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed44-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed44-126">CommonParameters</span></span>
<span data-ttu-id="0ed44-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0ed44-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed44-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ed44-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed44-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0ed44-129">INPUTS</span></span>

### <span data-ttu-id="0ed44-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0ed44-130">System.String</span></span>

## <span data-ttu-id="0ed44-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0ed44-131">OUTPUTS</span></span>

### <span data-ttu-id="0ed44-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0ed44-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0ed44-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0ed44-133">NOTES</span></span>

## <span data-ttu-id="0ed44-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ed44-134">RELATED LINKS</span></span>

<span data-ttu-id="0ed44-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="0ed44-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
