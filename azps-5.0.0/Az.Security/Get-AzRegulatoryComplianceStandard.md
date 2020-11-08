---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140912"
---
# <span data-ttu-id="5b6e7-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="5b6e7-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="5b6e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6e7-103">取得 regulatoey 規範標準</span><span class="sxs-lookup"><span data-stu-id="5b6e7-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="5b6e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b6e7-104">SYNTAX</span></span>

### <span data-ttu-id="5b6e7-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="5b6e7-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b6e7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="5b6e7-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b6e7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b6e7-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b6e7-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b6e7-108">DESCRIPTION</span></span>
<span data-ttu-id="5b6e7-109">取得 spcific 合規性 satandard 詳細資料，或列出特定訂閱下的所有規章規範標準。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="5b6e7-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b6e7-110">EXAMPLES</span></span>

### <span data-ttu-id="5b6e7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5b6e7-111">Example 1</span></span>
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

<span data-ttu-id="5b6e7-112">取得訂閱的所有規章遵從標準。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="5b6e7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5b6e7-113">Example 2</span></span>
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

<span data-ttu-id="5b6e7-114">根據標準名稱取得特定規章規範標準的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="5b6e7-115">範例3</span><span class="sxs-lookup"><span data-stu-id="5b6e7-115">Example 3</span></span>
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

<span data-ttu-id="5b6e7-116">根據資源識別碼取得特定規章規範標準的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="5b6e7-117">參數</span><span class="sxs-lookup"><span data-stu-id="5b6e7-117">PARAMETERS</span></span>

### <span data-ttu-id="5b6e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6e7-118">-DefaultProfile</span></span>
<span data-ttu-id="5b6e7-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b6e7-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b6e7-120">-Name</span></span>
<span data-ttu-id="5b6e7-121">標準名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-121">Standard name.</span></span>

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

### <span data-ttu-id="5b6e7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b6e7-122">-ResourceId</span></span>
<span data-ttu-id="5b6e7-123">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5b6e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6e7-124">CommonParameters</span></span>
<span data-ttu-id="5b6e7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6e7-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b6e7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6e7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5b6e7-127">INPUTS</span></span>

### <span data-ttu-id="5b6e7-128">System.object</span><span class="sxs-lookup"><span data-stu-id="5b6e7-128">System.String</span></span>

## <span data-ttu-id="5b6e7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5b6e7-129">OUTPUTS</span></span>

### <span data-ttu-id="5b6e7-130">SecurityCenter RegulatoryCompliance. PSSecurityRegulatoryComplianceStandard （）</span><span class="sxs-lookup"><span data-stu-id="5b6e7-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="5b6e7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5b6e7-131">NOTES</span></span>

## <span data-ttu-id="5b6e7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b6e7-132">RELATED LINKS</span></span>
