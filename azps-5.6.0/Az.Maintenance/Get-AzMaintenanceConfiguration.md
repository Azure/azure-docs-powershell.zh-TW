---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: 6939cde26695cb4273d776437c3697c03d426db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910081"
---
# <span data-ttu-id="592f3-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="592f3-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="592f3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="592f3-102">SYNOPSIS</span></span>
<span data-ttu-id="592f3-103">取得維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="592f3-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="592f3-104">語法</span><span class="sxs-lookup"><span data-stu-id="592f3-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="592f3-105">描述</span><span class="sxs-lookup"><span data-stu-id="592f3-105">DESCRIPTION</span></span>
<span data-ttu-id="592f3-106">取得維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="592f3-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="592f3-107">例子</span><span class="sxs-lookup"><span data-stu-id="592f3-107">EXAMPLES</span></span>

### <span data-ttu-id="592f3-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="592f3-108">Example 1</span></span>
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

<span data-ttu-id="592f3-109">取得維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="592f3-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="592f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="592f3-110">PARAMETERS</span></span>

### <span data-ttu-id="592f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592f3-111">-DefaultProfile</span></span>
<span data-ttu-id="592f3-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="592f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592f3-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="592f3-113">-Name</span></span>
<span data-ttu-id="592f3-114">維護組組名稱。</span><span class="sxs-lookup"><span data-stu-id="592f3-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="592f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="592f3-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="592f3-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="592f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592f3-117">CommonParameters</span></span>
<span data-ttu-id="592f3-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="592f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592f3-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="592f3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592f3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="592f3-120">INPUTS</span></span>

### <span data-ttu-id="592f3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="592f3-121">System.String</span></span>

## <span data-ttu-id="592f3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="592f3-122">OUTPUTS</span></span>

### <span data-ttu-id="592f3-123">Microsoft.Azure.Commands.Maintenance.models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="592f3-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="592f3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="592f3-124">NOTES</span></span>

## <span data-ttu-id="592f3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="592f3-125">RELATED LINKS</span></span>
