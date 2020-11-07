---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965670"
---
# <span data-ttu-id="4655a-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4655a-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="4655a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4655a-102">SYNOPSIS</span></span>
<span data-ttu-id="4655a-103">取得維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="4655a-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="4655a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4655a-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4655a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4655a-105">DESCRIPTION</span></span>
<span data-ttu-id="4655a-106">取得維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="4655a-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="4655a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4655a-107">EXAMPLES</span></span>

### <span data-ttu-id="4655a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4655a-108">Example 1</span></span>
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

<span data-ttu-id="4655a-109">取得維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="4655a-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="4655a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4655a-110">PARAMETERS</span></span>

### <span data-ttu-id="4655a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4655a-111">-DefaultProfile</span></span>
<span data-ttu-id="4655a-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4655a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4655a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4655a-113">-Name</span></span>
<span data-ttu-id="4655a-114">維護配置名稱。</span><span class="sxs-lookup"><span data-stu-id="4655a-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="4655a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4655a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4655a-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4655a-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="4655a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4655a-117">CommonParameters</span></span>
<span data-ttu-id="4655a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4655a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4655a-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4655a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4655a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4655a-120">INPUTS</span></span>

### <span data-ttu-id="4655a-121">System.object</span><span class="sxs-lookup"><span data-stu-id="4655a-121">System.String</span></span>

## <span data-ttu-id="4655a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4655a-122">OUTPUTS</span></span>

### <span data-ttu-id="4655a-123">PSMaintenanceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4655a-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="4655a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4655a-124">NOTES</span></span>

## <span data-ttu-id="4655a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="4655a-125">RELATED LINKS</span></span>
