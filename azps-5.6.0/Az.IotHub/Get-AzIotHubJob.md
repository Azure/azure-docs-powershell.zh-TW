---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 191b5a75a5f9f581308c8d5aa214fe4f2ae84851
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911046"
---
# <span data-ttu-id="732ad-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="732ad-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="732ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="732ad-102">SYNOPSIS</span></span>
<span data-ttu-id="732ad-103">獲得 IotHub 工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="732ad-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="732ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="732ad-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="732ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="732ad-105">DESCRIPTION</span></span>
<span data-ttu-id="732ad-106">獲得 IotHub 工作相關資訊。</span><span class="sxs-lookup"><span data-stu-id="732ad-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="732ad-107">使用命令或命令初始化匯New-AzIotHubExportDevices或匯出作業New-AzIotHubImportDevices IotHub Job。</span><span class="sxs-lookup"><span data-stu-id="732ad-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="732ad-108">您可以列出所有工作，或根據工作識別碼篩選工作。</span><span class="sxs-lookup"><span data-stu-id="732ad-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="732ad-109">例子</span><span class="sxs-lookup"><span data-stu-id="732ad-109">EXAMPLES</span></span>

### <span data-ttu-id="732ad-110">範例 1 列出所有工作</span><span class="sxs-lookup"><span data-stu-id="732ad-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="732ad-111">獲得名為"myiothub" 的 IotHub 的所有工作</span><span class="sxs-lookup"><span data-stu-id="732ad-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="732ad-112">範例 2 取得特定工作</span><span class="sxs-lookup"><span data-stu-id="732ad-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="732ad-113">使用識別碼 "3630fc31-4caa-43e8-a232-ea0577221cb2" 的識別碼為 "myiothub" 的工作相關資訊</span><span class="sxs-lookup"><span data-stu-id="732ad-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="732ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="732ad-114">PARAMETERS</span></span>

### <span data-ttu-id="732ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732ad-115">-DefaultProfile</span></span>
<span data-ttu-id="732ad-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="732ad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="732ad-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="732ad-117">-JobId</span></span>
<span data-ttu-id="732ad-118">工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="732ad-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="732ad-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="732ad-119">-Name</span></span>
<span data-ttu-id="732ad-120">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="732ad-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="732ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="732ad-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="732ad-122">Resource Group Name</span></span>

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

### <span data-ttu-id="732ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732ad-123">CommonParameters</span></span>
<span data-ttu-id="732ad-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="732ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732ad-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="732ad-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732ad-126">輸入</span><span class="sxs-lookup"><span data-stu-id="732ad-126">INPUTS</span></span>

### <span data-ttu-id="732ad-127">System.String</span><span class="sxs-lookup"><span data-stu-id="732ad-127">System.String</span></span>

## <span data-ttu-id="732ad-128">輸出</span><span class="sxs-lookup"><span data-stu-id="732ad-128">OUTPUTS</span></span>

### <span data-ttu-id="732ad-129">Microsoft.Azure.Commands.management.IotHub.models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="732ad-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="732ad-130">筆記</span><span class="sxs-lookup"><span data-stu-id="732ad-130">NOTES</span></span>

## <span data-ttu-id="732ad-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="732ad-131">RELATED LINKS</span></span>
