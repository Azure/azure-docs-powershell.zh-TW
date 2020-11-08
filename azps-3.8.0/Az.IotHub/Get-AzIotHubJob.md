---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957835"
---
# <span data-ttu-id="bf0e1-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="bf0e1-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="bf0e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0e1-103">取得 IotHub 工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="bf0e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf0e1-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf0e1-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf0e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bf0e1-106">取得 IotHub 工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="bf0e1-107">當您使用 New-AzIotHubExportDevices 或 New-AzIotHubImportDevices 命令初始化匯入或匯出作業時，就會建立 IotHub 工作。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="bf0e1-108">您可以依作業識別碼列出所有作業或篩選作業。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="bf0e1-109">示例</span><span class="sxs-lookup"><span data-stu-id="bf0e1-109">EXAMPLES</span></span>

### <span data-ttu-id="bf0e1-110">範例1列出所有工作</span><span class="sxs-lookup"><span data-stu-id="bf0e1-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bf0e1-111">取得名為 "myiothub" 的 IotHub 的所有工作</span><span class="sxs-lookup"><span data-stu-id="bf0e1-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="bf0e1-112">範例2取得特定工作</span><span class="sxs-lookup"><span data-stu-id="bf0e1-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="bf0e1-113">取得名為 "3630fc31-4caa-43e8-a232-ea0577221cb2" 的 IotHub 的工作相關資訊 [myiothub "</span><span class="sxs-lookup"><span data-stu-id="bf0e1-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bf0e1-114">參數</span><span class="sxs-lookup"><span data-stu-id="bf0e1-114">PARAMETERS</span></span>

### <span data-ttu-id="bf0e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0e1-115">-DefaultProfile</span></span>
<span data-ttu-id="bf0e1-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bf0e1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf0e1-117">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="bf0e1-117">-JobId</span></span>
<span data-ttu-id="bf0e1-118">作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf0e1-119">-Name</span></span>
<span data-ttu-id="bf0e1-120">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-120">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0e1-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf0e1-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bf0e1-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0e1-123">CommonParameters</span></span>
<span data-ttu-id="bf0e1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0e1-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0e1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="bf0e1-126">INPUTS</span></span>

### <span data-ttu-id="bf0e1-127">System.object</span><span class="sxs-lookup"><span data-stu-id="bf0e1-127">System.String</span></span>

## <span data-ttu-id="bf0e1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="bf0e1-128">OUTPUTS</span></span>

### <span data-ttu-id="bf0e1-129">PSIotHubJobResponse （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bf0e1-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="bf0e1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="bf0e1-130">NOTES</span></span>

## <span data-ttu-id="bf0e1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf0e1-131">RELATED LINKS</span></span>