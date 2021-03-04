---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: a4625d48086064fb59b5f2faee78357380f6a323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914765"
---
# <span data-ttu-id="3e50f-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e50f-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="3e50f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e50f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e50f-103">取得公用維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="3e50f-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="3e50f-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e50f-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e50f-105">描述</span><span class="sxs-lookup"><span data-stu-id="3e50f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e50f-106">取得公用維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="3e50f-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="3e50f-107">例子</span><span class="sxs-lookup"><span data-stu-id="3e50f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e50f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3e50f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="3e50f-109">取得公用維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="3e50f-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="3e50f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e50f-110">PARAMETERS</span></span>

### <span data-ttu-id="3e50f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e50f-111">-DefaultProfile</span></span>
<span data-ttu-id="3e50f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e50f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e50f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e50f-113">-Name</span></span>
<span data-ttu-id="3e50f-114">公用維護組組名。</span><span class="sxs-lookup"><span data-stu-id="3e50f-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e50f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e50f-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e50f-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e50f-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e50f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e50f-117">CommonParameters</span></span>
<span data-ttu-id="3e50f-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e50f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e50f-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e50f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e50f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="3e50f-120">INPUTS</span></span>

### <span data-ttu-id="3e50f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="3e50f-121">System.String</span></span>

## <span data-ttu-id="3e50f-122">輸出</span><span class="sxs-lookup"><span data-stu-id="3e50f-122">OUTPUTS</span></span>

### <span data-ttu-id="3e50f-123">Microsoft.Azure.Commands.Maintenance.models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e50f-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="3e50f-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3e50f-124">NOTES</span></span>

## <span data-ttu-id="3e50f-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e50f-125">RELATED LINKS</span></span>
