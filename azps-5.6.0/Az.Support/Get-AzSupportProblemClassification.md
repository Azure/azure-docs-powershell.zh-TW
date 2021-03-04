---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: 0c8bf7d7a8217ed63920495591f8ad061f1b0a8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907046"
---
# <span data-ttu-id="75339-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="75339-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="75339-102">簡介</span><span class="sxs-lookup"><span data-stu-id="75339-102">SYNOPSIS</span></span>
<span data-ttu-id="75339-103">取得指定服務的問題分類。</span><span class="sxs-lookup"><span data-stu-id="75339-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="75339-104">語法</span><span class="sxs-lookup"><span data-stu-id="75339-104">SYNTAX</span></span>

### <span data-ttu-id="75339-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="75339-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75339-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75339-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75339-107">描述</span><span class="sxs-lookup"><span data-stu-id="75339-107">DESCRIPTION</span></span>
<span data-ttu-id="75339-108">獲得 Azure 服務目前的問題分類清單。</span><span class="sxs-lookup"><span data-stu-id="75339-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="75339-109">您可以使用服務和問題分類 GUID，使用 New-AzSupportTicket 建立新的支援票證。</span><span class="sxs-lookup"><span data-stu-id="75339-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="75339-110">一直使用以程式化方式取得的服務與問題分類 GUID。</span><span class="sxs-lookup"><span data-stu-id="75339-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="75339-111">此做法可確保您擁有最新的一組服務與問題分類 GUID，以建立支援票證。</span><span class="sxs-lookup"><span data-stu-id="75339-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="75339-112">例子</span><span class="sxs-lookup"><span data-stu-id="75339-112">EXAMPLES</span></span>

### <span data-ttu-id="75339-113">範例 1：使用服務識別碼參數取得服務的所有問題類別。</span><span class="sxs-lookup"><span data-stu-id="75339-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
```powershell
PS C:\> Get-AzSupportProblemClassification -ServiceId "{vm_running_windows_service_guid}"

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="75339-114">範例 2：使用父服務物件取得服務的所有問題類別</span><span class="sxs-lookup"><span data-stu-id="75339-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification 

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="75339-115">範例 3：取得單一問題類別，以 id 根據管道服務物件取得詳細資料</span><span class="sxs-lookup"><span data-stu-id="75339-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="75339-116">參數</span><span class="sxs-lookup"><span data-stu-id="75339-116">PARAMETERS</span></span>

### <span data-ttu-id="75339-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75339-117">-DefaultProfile</span></span>
<span data-ttu-id="75339-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="75339-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75339-119">-Id</span><span class="sxs-lookup"><span data-stu-id="75339-119">-Id</span></span>
<span data-ttu-id="75339-120">問題分類識別碼。</span><span class="sxs-lookup"><span data-stu-id="75339-120">Problem classification id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75339-121">-ServiceId</span><span class="sxs-lookup"><span data-stu-id="75339-121">-ServiceId</span></span>
<span data-ttu-id="75339-122">已針對所有問題分類所取取的服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="75339-122">Service id for which all problem classifications are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75339-123">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="75339-123">-ServiceObject</span></span>
<span data-ttu-id="75339-124">已取回分類問題的服務物件。</span><span class="sxs-lookup"><span data-stu-id="75339-124">Service object for which problem classifications are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportService
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75339-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75339-125">CommonParameters</span></span>
<span data-ttu-id="75339-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="75339-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75339-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75339-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75339-128">輸入</span><span class="sxs-lookup"><span data-stu-id="75339-128">INPUTS</span></span>

### <span data-ttu-id="75339-129">Microsoft.Azure.Commands.support.models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="75339-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="75339-130">輸出</span><span class="sxs-lookup"><span data-stu-id="75339-130">OUTPUTS</span></span>

### <span data-ttu-id="75339-131">Microsoft.Azure.Commands.support.models.PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="75339-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="75339-132">筆記</span><span class="sxs-lookup"><span data-stu-id="75339-132">NOTES</span></span>

## <span data-ttu-id="75339-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="75339-133">RELATED LINKS</span></span>
