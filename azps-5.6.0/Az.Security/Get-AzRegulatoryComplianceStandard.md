---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: c13b4ed784f37e9b01bc8cf5dd618d97305a95d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916500"
---
# <span data-ttu-id="2d205-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="2d205-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="2d205-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d205-102">SYNOPSIS</span></span>
<span data-ttu-id="2d205-103">獲得 regulatoey 合規性標準</span><span class="sxs-lookup"><span data-stu-id="2d205-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="2d205-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d205-104">SYNTAX</span></span>

### <span data-ttu-id="2d205-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="2d205-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d205-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2d205-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d205-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d205-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d205-108">描述</span><span class="sxs-lookup"><span data-stu-id="2d205-108">DESCRIPTION</span></span>
<span data-ttu-id="2d205-109">取得詳細的法規合規性詳細資料，或列出特定訂閱下的所有法規合規性標準。</span><span class="sxs-lookup"><span data-stu-id="2d205-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="2d205-110">例子</span><span class="sxs-lookup"><span data-stu-id="2d205-110">EXAMPLES</span></span>

### <span data-ttu-id="2d205-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2d205-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2d205-112">取得訂閱下的所有法規合規性標準。</span><span class="sxs-lookup"><span data-stu-id="2d205-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="2d205-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="2d205-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2d205-114">根據標準名稱取得特定法規合規性標準的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2d205-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="2d205-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="2d205-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2d205-116">根據資源識別碼取得特定法規合規性標準的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2d205-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="2d205-117">參數</span><span class="sxs-lookup"><span data-stu-id="2d205-117">PARAMETERS</span></span>

### <span data-ttu-id="2d205-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d205-118">-DefaultProfile</span></span>
<span data-ttu-id="2d205-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d205-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d205-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d205-120">-Name</span></span>
<span data-ttu-id="2d205-121">標準名稱。</span><span class="sxs-lookup"><span data-stu-id="2d205-121">Standard name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d205-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d205-122">-ResourceId</span></span>
<span data-ttu-id="2d205-123">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d205-123">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d205-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d205-124">CommonParameters</span></span>
<span data-ttu-id="2d205-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d205-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d205-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d205-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d205-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2d205-127">INPUTS</span></span>

### <span data-ttu-id="2d205-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2d205-128">System.String</span></span>

## <span data-ttu-id="2d205-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2d205-129">OUTPUTS</span></span>

### <span data-ttu-id="2d205-130">Microsoft.Azure.Commands.SecurityCenter.models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="2d205-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="2d205-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2d205-131">NOTES</span></span>

## <span data-ttu-id="2d205-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d205-132">RELATED LINKS</span></span>
