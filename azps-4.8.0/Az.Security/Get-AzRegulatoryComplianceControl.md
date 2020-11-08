---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128099"
---
# <span data-ttu-id="5a508-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="5a508-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="5a508-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a508-102">SYNOPSIS</span></span>
<span data-ttu-id="5a508-103">取得管制規範控制措施</span><span class="sxs-lookup"><span data-stu-id="5a508-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="5a508-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a508-104">SYNTAX</span></span>

### <span data-ttu-id="5a508-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="5a508-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a508-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a508-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a508-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a508-107">DESCRIPTION</span></span>
<span data-ttu-id="5a508-108">取得特定規章規範標準底下的 spcific 控制項詳細資料或清單控制項。</span><span class="sxs-lookup"><span data-stu-id="5a508-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="5a508-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a508-109">EXAMPLES</span></span>

### <span data-ttu-id="5a508-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5a508-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="5a508-111">取得特定規章標準下的所有控制項。</span><span class="sxs-lookup"><span data-stu-id="5a508-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="5a508-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5a508-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="5a508-113">根據控制項識別碼取得特定控制項的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5a508-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="5a508-114">範例3</span><span class="sxs-lookup"><span data-stu-id="5a508-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="5a508-115">根據資源識別碼取得特定的控制項詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5a508-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="5a508-116">參數</span><span class="sxs-lookup"><span data-stu-id="5a508-116">PARAMETERS</span></span>

### <span data-ttu-id="5a508-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a508-117">-DefaultProfile</span></span>
<span data-ttu-id="5a508-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a508-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a508-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a508-119">-Name</span></span>
<span data-ttu-id="5a508-120">控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a508-120">Control Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a508-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a508-121">-ResourceId</span></span>
<span data-ttu-id="5a508-122">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a508-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5a508-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="5a508-123">-StandardName</span></span>
<span data-ttu-id="5a508-124">標準名稱。</span><span class="sxs-lookup"><span data-stu-id="5a508-124">Standard Name.</span></span>

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

### <span data-ttu-id="5a508-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a508-125">CommonParameters</span></span>
<span data-ttu-id="5a508-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a508-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a508-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a508-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a508-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5a508-128">INPUTS</span></span>

### <span data-ttu-id="5a508-129">System.object</span><span class="sxs-lookup"><span data-stu-id="5a508-129">System.String</span></span>

## <span data-ttu-id="5a508-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5a508-130">OUTPUTS</span></span>

### <span data-ttu-id="5a508-131">SecurityCenter RegulatoryCompliance. PSSecurityRegulatoryComplianceControl （）</span><span class="sxs-lookup"><span data-stu-id="5a508-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="5a508-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5a508-132">NOTES</span></span>

## <span data-ttu-id="5a508-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a508-133">RELATED LINKS</span></span>
