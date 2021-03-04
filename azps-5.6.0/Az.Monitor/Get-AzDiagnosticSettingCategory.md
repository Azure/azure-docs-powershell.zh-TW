---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: df263698a913faf361e5f23bb12d0267be314106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908937"
---
# <span data-ttu-id="b621b-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="b621b-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="b621b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b621b-102">SYNOPSIS</span></span>
<span data-ttu-id="b621b-103">取得或列出 Azure 資源支援的診斷設定類別。</span><span class="sxs-lookup"><span data-stu-id="b621b-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="b621b-104">語法</span><span class="sxs-lookup"><span data-stu-id="b621b-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b621b-105">描述</span><span class="sxs-lookup"><span data-stu-id="b621b-105">DESCRIPTION</span></span>
<span data-ttu-id="b621b-106">取得或列出 Azure 資源支援的診斷設定類別。</span><span class="sxs-lookup"><span data-stu-id="b621b-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="b621b-107">例子</span><span class="sxs-lookup"><span data-stu-id="b621b-107">EXAMPLES</span></span>

### <span data-ttu-id="b621b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b621b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="b621b-109">取得支援之虛擬網路的診斷設定類別。</span><span class="sxs-lookup"><span data-stu-id="b621b-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="b621b-110">參數</span><span class="sxs-lookup"><span data-stu-id="b621b-110">PARAMETERS</span></span>

### <span data-ttu-id="b621b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b621b-111">-DefaultProfile</span></span>
<span data-ttu-id="b621b-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b621b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b621b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b621b-113">-Name</span></span>
<span data-ttu-id="b621b-114">診斷設定類別的名稱</span><span class="sxs-lookup"><span data-stu-id="b621b-114">Name of diagnostic setting category</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b621b-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b621b-115">-TargetResourceId</span></span>
<span data-ttu-id="b621b-116">目標資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b621b-116">Target resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b621b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b621b-117">CommonParameters</span></span>
<span data-ttu-id="b621b-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b621b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b621b-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b621b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b621b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b621b-120">INPUTS</span></span>

### <span data-ttu-id="b621b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b621b-121">System.String</span></span>

## <span data-ttu-id="b621b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b621b-122">OUTPUTS</span></span>

### <span data-ttu-id="b621b-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="b621b-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="b621b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b621b-124">NOTES</span></span>

## <span data-ttu-id="b621b-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b621b-125">RELATED LINKS</span></span>
