---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138800"
---
# <span data-ttu-id="e49fa-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="e49fa-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="e49fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e49fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e49fa-103">取得公用維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="e49fa-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="e49fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="e49fa-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e49fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="e49fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e49fa-106">取得公用維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="e49fa-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="e49fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="e49fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e49fa-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e49fa-108">Example 1</span></span>
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

<span data-ttu-id="e49fa-109">取得公用維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="e49fa-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="e49fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="e49fa-110">PARAMETERS</span></span>

### <span data-ttu-id="e49fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49fa-111">-DefaultProfile</span></span>
<span data-ttu-id="e49fa-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e49fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49fa-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e49fa-113">-Name</span></span>
<span data-ttu-id="e49fa-114">公用維護配置名稱。</span><span class="sxs-lookup"><span data-stu-id="e49fa-114">The public maintenance configuration Name.</span></span>

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

### <span data-ttu-id="e49fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="e49fa-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e49fa-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="e49fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49fa-117">CommonParameters</span></span>
<span data-ttu-id="e49fa-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e49fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49fa-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e49fa-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49fa-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e49fa-120">INPUTS</span></span>

### <span data-ttu-id="e49fa-121">System.object</span><span class="sxs-lookup"><span data-stu-id="e49fa-121">System.String</span></span>

## <span data-ttu-id="e49fa-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e49fa-122">OUTPUTS</span></span>

### <span data-ttu-id="e49fa-123">PSMaintenanceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e49fa-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e49fa-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e49fa-124">NOTES</span></span>

## <span data-ttu-id="e49fa-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e49fa-125">RELATED LINKS</span></span>