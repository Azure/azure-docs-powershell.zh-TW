---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 2d1c4b2f272516af31fba17db50d33991dd1db50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439143"
---
# <span data-ttu-id="500de-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="500de-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="500de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="500de-102">SYNOPSIS</span></span>
<span data-ttu-id="500de-103">取得或列出 Azure 資源支援的診斷設定類別。</span><span class="sxs-lookup"><span data-stu-id="500de-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="500de-104">句法</span><span class="sxs-lookup"><span data-stu-id="500de-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="500de-105">說明</span><span class="sxs-lookup"><span data-stu-id="500de-105">DESCRIPTION</span></span>
<span data-ttu-id="500de-106">取得或列出 Azure 資源支援的診斷設定類別。</span><span class="sxs-lookup"><span data-stu-id="500de-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="500de-107">示例</span><span class="sxs-lookup"><span data-stu-id="500de-107">EXAMPLES</span></span>

### <span data-ttu-id="500de-108">範例1</span><span class="sxs-lookup"><span data-stu-id="500de-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSetting -TargetResourceId -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="500de-109">取得虛擬網路支援的診斷設定類別。</span><span class="sxs-lookup"><span data-stu-id="500de-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="500de-110">參數</span><span class="sxs-lookup"><span data-stu-id="500de-110">PARAMETERS</span></span>

### <span data-ttu-id="500de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500de-111">-DefaultProfile</span></span>
<span data-ttu-id="500de-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="500de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500de-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="500de-113">-Name</span></span>
<span data-ttu-id="500de-114">診斷設定類別的名稱</span><span class="sxs-lookup"><span data-stu-id="500de-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="500de-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="500de-115">-TargetResourceId</span></span>
<span data-ttu-id="500de-116">目標資源識別碼</span><span class="sxs-lookup"><span data-stu-id="500de-116">Target resource Id</span></span>

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

### <span data-ttu-id="500de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500de-117">CommonParameters</span></span>
<span data-ttu-id="500de-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="500de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500de-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="500de-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500de-120">輸入</span><span class="sxs-lookup"><span data-stu-id="500de-120">INPUTS</span></span>

### <span data-ttu-id="500de-121">System.object</span><span class="sxs-lookup"><span data-stu-id="500de-121">System.String</span></span>

## <span data-ttu-id="500de-122">輸出</span><span class="sxs-lookup"><span data-stu-id="500de-122">OUTPUTS</span></span>

### <span data-ttu-id="500de-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="500de-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="500de-124">筆記</span><span class="sxs-lookup"><span data-stu-id="500de-124">NOTES</span></span>

## <span data-ttu-id="500de-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="500de-125">RELATED LINKS</span></span>
