---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: 951cb486495a56eb6d1d74c159df20ac6da8c324
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795505"
---
# <span data-ttu-id="cf9ec-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cf9ec-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="cf9ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9ec-103">移除 a 資源的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="cf9ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf9ec-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf9ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="cf9ec-106">**AzDiagnosticSetting** Cmdlet 會移除特定資源的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="cf9ec-107">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="cf9ec-108">示例</span><span class="sxs-lookup"><span data-stu-id="cf9ec-108">EXAMPLES</span></span>

### <span data-ttu-id="cf9ec-109">範例1：移除資源的預設診斷設定 (服務) </span><span class="sxs-lookup"><span data-stu-id="cf9ec-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="cf9ec-110">這個命令會移除稱為 Resource01 之資源的預設診斷設定 (服務) 。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="cf9ec-111">範例2：移除資源指定名稱所識別的預設診斷設定</span><span class="sxs-lookup"><span data-stu-id="cf9ec-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="cf9ec-112">這個命令會針對稱為 Resource01 的資源，移除稱為 myDiagSetting 的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="cf9ec-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf9ec-113">PARAMETERS</span></span>

### <span data-ttu-id="cf9ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9ec-114">-DefaultProfile</span></span>
<span data-ttu-id="cf9ec-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf9ec-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf9ec-116">-Name</span></span>
<span data-ttu-id="cf9ec-117">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="cf9ec-118">如果未指定呼叫預設為「服務」，就像在舊版 API 中一樣，這個 Cmdlet 只會停用所有類別的指標/記錄。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="cf9ec-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf9ec-119">-ResourceId</span></span>
<span data-ttu-id="cf9ec-120">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="cf9ec-121">-確認</span><span class="sxs-lookup"><span data-stu-id="cf9ec-121">-Confirm</span></span>
<span data-ttu-id="cf9ec-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf9ec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf9ec-123">-WhatIf</span></span>
<span data-ttu-id="cf9ec-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf9ec-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf9ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9ec-126">CommonParameters</span></span>
<span data-ttu-id="cf9ec-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9ec-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf9ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9ec-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cf9ec-129">INPUTS</span></span>

### <span data-ttu-id="cf9ec-130">System.object</span><span class="sxs-lookup"><span data-stu-id="cf9ec-130">System.String</span></span>

## <span data-ttu-id="cf9ec-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cf9ec-131">OUTPUTS</span></span>

### <span data-ttu-id="cf9ec-132">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cf9ec-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="cf9ec-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cf9ec-133">NOTES</span></span>

## <span data-ttu-id="cf9ec-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf9ec-134">RELATED LINKS</span></span>

<span data-ttu-id="cf9ec-135">[AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="cf9ec-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
