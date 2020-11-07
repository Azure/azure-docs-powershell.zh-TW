---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
ms.openlocfilehash: 019f37fa6b735b506c71a914a6ea59700565fd49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797821"
---
# <span data-ttu-id="22b26-101">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="22b26-101">Get-AzSupportService</span></span>

## <span data-ttu-id="22b26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22b26-102">SYNOPSIS</span></span>
<span data-ttu-id="22b26-103">取得可供使用的支援服務。</span><span class="sxs-lookup"><span data-stu-id="22b26-103">Get services for which support is available.</span></span> 

## <span data-ttu-id="22b26-104">句法</span><span class="sxs-lookup"><span data-stu-id="22b26-104">SYNTAX</span></span>

### <span data-ttu-id="22b26-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22b26-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportService [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22b26-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22b26-106">GetByNameParameterSet</span></span>
```
Get-AzSupportService -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b26-107">說明</span><span class="sxs-lookup"><span data-stu-id="22b26-107">DESCRIPTION</span></span>
<span data-ttu-id="22b26-108">取得目前提供支援的 Azure 服務清單。</span><span class="sxs-lookup"><span data-stu-id="22b26-108">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="22b26-109">每個服務都可能包含一或多個 Azure 資源管理員 (ARM) 資源類型資訊。</span><span class="sxs-lookup"><span data-stu-id="22b26-109">Each service may contain one or more Azure resource manager (ARM) resource type information.</span></span> <span data-ttu-id="22b26-110">資源類型 (範例：「"microsoft. compute/virtualmachines" ) 在建立技術支援票證時，對應正確的產品和 ARM 資源是很有用的。</span><span class="sxs-lookup"><span data-stu-id="22b26-110">Resource types (example: 'microsoft.compute/virtualmachines') can be useful to map the right product and ARM resource when creating a technical support ticket.</span></span> <span data-ttu-id="22b26-111">每個 Azure 服務都有自己的一組類別，稱為「問題分類」。</span><span class="sxs-lookup"><span data-stu-id="22b26-111">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="22b26-112">使用 AzSupportProblemClassification，以取得服務的目前問題分類清單。</span><span class="sxs-lookup"><span data-stu-id="22b26-112">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="22b26-113">您可以使用 [服務] 和 [問題分類 GUID]，使用新的 AzSupportTicket 建立新的支援票證。</span><span class="sxs-lookup"><span data-stu-id="22b26-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="22b26-114">永遠使用以程式設計方式取得的服務和問題分類 Guid。</span><span class="sxs-lookup"><span data-stu-id="22b26-114">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="22b26-115">這項做法可確保您擁有最新的一組服務和問題分類 Guid 來建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="22b26-115">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="22b26-116">示例</span><span class="sxs-lookup"><span data-stu-id="22b26-116">EXAMPLES</span></span>

### <span data-ttu-id="22b26-117">範例1：取得所有可供支援的服務</span><span class="sxs-lookup"><span data-stu-id="22b26-117">Example 1: Get all services available for support</span></span>
```powershell
PS C:\> Get-AzSupportService

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
809e8afe-489e-08b0-95f2-08f835a383e8 Advanced Threat Protection - Azure
6859f4e8-4a1d-13e4-f276-6d055007e83d Advanced Threat Protection - Microsoft Defender
94332e54-73b0-b8e3-306e-db3ad13d950b Advanced Threat Protection - O365
26d8424b-0a41-4443-cbc6-0309ea8708d0 Advisor
8f1ddc5f-0c5e-50c7-9810-e01a8d1da925 AKS Engine on Azure Stack
c1840ac9-309f-f235-c0ae-4782f283b698 Alerts and Action Groups
e8fe7c6f-d883-c57f-6576-cf801ca30653 Analysis Services
07651e65-958a-0877-36f3-61bbba85d783 API for FHIR
b4d0e877-0166-0474-9a76-b5be30ba40e4 API Management Service
e14f616b-42c5-4515-3d7c-67935eece51a App Configuration
445c0905-55e2-4f42-d853-ec9e17a5180e App Service Certificates
b7d2f8b7-7d20-cf2f-ddd5-5543ada54bd2 App Service Domains
101732bb-31af-ee61-7c16-d4ad77c86a50 Application Gateway
```

### <span data-ttu-id="22b26-118">範例2：取得單一服務的詳細資料（依 id 提供支援）</span><span class="sxs-lookup"><span data-stu-id="22b26-118">Example 2: Get details of a single service by id available for support</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "484e2236-bc6d-b1bb-76d2-7d09278cf9ea"

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
```

## <span data-ttu-id="22b26-119">參數</span><span class="sxs-lookup"><span data-stu-id="22b26-119">PARAMETERS</span></span>

### <span data-ttu-id="22b26-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b26-120">-DefaultProfile</span></span>
<span data-ttu-id="22b26-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22b26-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b26-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="22b26-122">-Id</span></span>
<span data-ttu-id="22b26-123">[服務識別碼]。</span><span class="sxs-lookup"><span data-stu-id="22b26-123">Service id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22b26-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b26-124">CommonParameters</span></span>
<span data-ttu-id="22b26-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22b26-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b26-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="22b26-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b26-127">輸入</span><span class="sxs-lookup"><span data-stu-id="22b26-127">INPUTS</span></span>

### <span data-ttu-id="22b26-128">所有</span><span class="sxs-lookup"><span data-stu-id="22b26-128">None</span></span>

## <span data-ttu-id="22b26-129">輸出</span><span class="sxs-lookup"><span data-stu-id="22b26-129">OUTPUTS</span></span>

### <span data-ttu-id="22b26-130">PSSupportService （支援）。</span><span class="sxs-lookup"><span data-stu-id="22b26-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="22b26-131">筆記</span><span class="sxs-lookup"><span data-stu-id="22b26-131">NOTES</span></span>

## <span data-ttu-id="22b26-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="22b26-132">RELATED LINKS</span></span>
