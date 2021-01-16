---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276728"
---
# <span data-ttu-id="739bd-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="739bd-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="739bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="739bd-102">SYNOPSIS</span></span>
<span data-ttu-id="739bd-103">取得維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="739bd-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="739bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="739bd-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="739bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="739bd-105">DESCRIPTION</span></span>
<span data-ttu-id="739bd-106">取得維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="739bd-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="739bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="739bd-107">EXAMPLES</span></span>

### <span data-ttu-id="739bd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="739bd-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="739bd-109">取得維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="739bd-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="739bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="739bd-110">PARAMETERS</span></span>

### <span data-ttu-id="739bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="739bd-111">-DefaultProfile</span></span>
<span data-ttu-id="739bd-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="739bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="739bd-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="739bd-113">-Name</span></span>
<span data-ttu-id="739bd-114">維護配置名稱。</span><span class="sxs-lookup"><span data-stu-id="739bd-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="739bd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="739bd-115">-ResourceGroupName</span></span>
<span data-ttu-id="739bd-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="739bd-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="739bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="739bd-117">CommonParameters</span></span>
<span data-ttu-id="739bd-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="739bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="739bd-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="739bd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="739bd-120">輸入</span><span class="sxs-lookup"><span data-stu-id="739bd-120">INPUTS</span></span>

### <span data-ttu-id="739bd-121">System.object</span><span class="sxs-lookup"><span data-stu-id="739bd-121">System.String</span></span>

## <span data-ttu-id="739bd-122">輸出</span><span class="sxs-lookup"><span data-stu-id="739bd-122">OUTPUTS</span></span>

### <span data-ttu-id="739bd-123">PSMaintenanceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="739bd-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="739bd-124">筆記</span><span class="sxs-lookup"><span data-stu-id="739bd-124">NOTES</span></span>

## <span data-ttu-id="739bd-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="739bd-125">RELATED LINKS</span></span>
