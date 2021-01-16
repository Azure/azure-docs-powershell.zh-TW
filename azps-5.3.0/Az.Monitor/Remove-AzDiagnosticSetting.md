---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288779"
---
# <span data-ttu-id="b7e70-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b7e70-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="b7e70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7e70-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e70-103">移除 a 資源的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="b7e70-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="b7e70-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7e70-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7e70-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7e70-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e70-106">**AzDiagnosticSetting** Cmdlet 會移除特定資源的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="b7e70-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="b7e70-107">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7e70-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b7e70-108">示例</span><span class="sxs-lookup"><span data-stu-id="b7e70-108">EXAMPLES</span></span>

### <span data-ttu-id="b7e70-109">範例1：移除資源的預設診斷設定 (服務) </span><span class="sxs-lookup"><span data-stu-id="b7e70-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="b7e70-110">這個命令會移除稱為 Resource01 之資源的預設診斷設定 (服務) 。</span><span class="sxs-lookup"><span data-stu-id="b7e70-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="b7e70-111">範例2：移除資源指定名稱所識別的預設診斷設定</span><span class="sxs-lookup"><span data-stu-id="b7e70-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="b7e70-112">這個命令會針對稱為 Resource01 的資源，移除稱為 myDiagSetting 的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="b7e70-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="b7e70-113">參數</span><span class="sxs-lookup"><span data-stu-id="b7e70-113">PARAMETERS</span></span>

### <span data-ttu-id="b7e70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e70-114">-DefaultProfile</span></span>
<span data-ttu-id="b7e70-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7e70-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7e70-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7e70-116">-Name</span></span>
<span data-ttu-id="b7e70-117">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7e70-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="b7e70-118">如果未指定呼叫預設為「服務」，就像在舊版 API 中一樣，這個 Cmdlet 只會停用所有類別的指標/記錄。</span><span class="sxs-lookup"><span data-stu-id="b7e70-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="b7e70-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7e70-119">-ResourceId</span></span>
<span data-ttu-id="b7e70-120">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7e70-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="b7e70-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b7e70-121">-Confirm</span></span>
<span data-ttu-id="b7e70-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7e70-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e70-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e70-123">-WhatIf</span></span>
<span data-ttu-id="b7e70-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7e70-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7e70-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7e70-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e70-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e70-126">CommonParameters</span></span>
<span data-ttu-id="b7e70-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7e70-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e70-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b7e70-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e70-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b7e70-129">INPUTS</span></span>

### <span data-ttu-id="b7e70-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b7e70-130">System.String</span></span>

## <span data-ttu-id="b7e70-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b7e70-131">OUTPUTS</span></span>

### <span data-ttu-id="b7e70-132">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b7e70-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b7e70-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b7e70-133">NOTES</span></span>

## <span data-ttu-id="b7e70-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7e70-134">RELATED LINKS</span></span>

<span data-ttu-id="b7e70-135">[AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="b7e70-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
