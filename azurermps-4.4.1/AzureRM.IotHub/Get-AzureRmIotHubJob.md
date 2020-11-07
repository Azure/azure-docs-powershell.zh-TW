---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: b0ea6f3cae3fe978a3d24b055eb47693ea466272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625172"
---
# <span data-ttu-id="6b823-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="6b823-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="6b823-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b823-102">SYNOPSIS</span></span>
<span data-ttu-id="6b823-103">取得 IotHub 工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6b823-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b823-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b823-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b823-105">說明</span><span class="sxs-lookup"><span data-stu-id="6b823-105">DESCRIPTION</span></span>
<span data-ttu-id="6b823-106">取得 IotHub 工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6b823-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="6b823-107">當您使用 New-AzureRmIotHubExportDevices 或 New-AzureRmIotHubImportDevices 命令 initialted 匯入或匯出作業時，就會建立 IotHub 工作。</span><span class="sxs-lookup"><span data-stu-id="6b823-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="6b823-108">您可以依作業識別碼列出所有作業或篩選作業。</span><span class="sxs-lookup"><span data-stu-id="6b823-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="6b823-109">示例</span><span class="sxs-lookup"><span data-stu-id="6b823-109">EXAMPLES</span></span>

### <span data-ttu-id="6b823-110">範例1列出所有工作</span><span class="sxs-lookup"><span data-stu-id="6b823-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6b823-111">取得名為 "myiothub" 的 IotHub 的所有工作</span><span class="sxs-lookup"><span data-stu-id="6b823-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="6b823-112">範例2取得特定工作</span><span class="sxs-lookup"><span data-stu-id="6b823-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="6b823-113">取得名為 "3630fc31-4caa-43e8-a232-ea0577221cb2" 的 IotHub 的工作相關資訊 [myiothub "</span><span class="sxs-lookup"><span data-stu-id="6b823-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="6b823-114">參數</span><span class="sxs-lookup"><span data-stu-id="6b823-114">PARAMETERS</span></span>

### <span data-ttu-id="6b823-115">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="6b823-115">-JobId</span></span>
<span data-ttu-id="6b823-116">作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b823-116">The Job Identifier.</span></span> 

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

### <span data-ttu-id="6b823-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b823-117">-Name</span></span>
<span data-ttu-id="6b823-118">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b823-118">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="6b823-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b823-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b823-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6b823-120">Resource Group Name</span></span>

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

### <span data-ttu-id="6b823-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b823-121">-DefaultProfile</span></span>
<span data-ttu-id="6b823-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b823-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b823-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b823-123">CommonParameters</span></span>
<span data-ttu-id="6b823-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b823-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b823-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b823-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b823-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6b823-126">INPUTS</span></span>

### <span data-ttu-id="6b823-127">System.object</span><span class="sxs-lookup"><span data-stu-id="6b823-127">System.String</span></span>

## <span data-ttu-id="6b823-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6b823-128">OUTPUTS</span></span>

### <span data-ttu-id="6b823-129">PSIotHubJobResponse （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="6b823-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="6b823-130">\` \[ \[ PSIotHubJobResponse、IotHub = 1.0.0.0、Culture = 中性、PublicKeyToken = null、Culture = 中立、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="6b823-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="6b823-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6b823-131">NOTES</span></span>

## <span data-ttu-id="6b823-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b823-132">RELATED LINKS</span></span>

