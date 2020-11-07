---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967955"
---
# <span data-ttu-id="03595-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="03595-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="03595-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03595-102">SYNOPSIS</span></span>
<span data-ttu-id="03595-103">取得網站的部署。</span><span class="sxs-lookup"><span data-stu-id="03595-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="03595-104">句法</span><span class="sxs-lookup"><span data-stu-id="03595-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="03595-105">說明</span><span class="sxs-lookup"><span data-stu-id="03595-105">DESCRIPTION</span></span>
<span data-ttu-id="03595-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03595-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="03595-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="03595-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="03595-108">取得 Azure 中網站的部署。</span><span class="sxs-lookup"><span data-stu-id="03595-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="03595-109">示例</span><span class="sxs-lookup"><span data-stu-id="03595-109">EXAMPLES</span></span>

## <span data-ttu-id="03595-110">參數</span><span class="sxs-lookup"><span data-stu-id="03595-110">PARAMETERS</span></span>

### <span data-ttu-id="03595-111">-CommitId</span><span class="sxs-lookup"><span data-stu-id="03595-111">-CommitId</span></span>
<span data-ttu-id="03595-112">指定部署的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="03595-112">Specifies the unique ID for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03595-113">-詳細資料</span><span class="sxs-lookup"><span data-stu-id="03595-113">-Details</span></span>
<span data-ttu-id="03595-114">顯示有關部署的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="03595-114">Shows detailed information about the deployments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03595-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="03595-115">-MaxResults</span></span>
<span data-ttu-id="03595-116">指定您想要命令傳回的結果數目。</span><span class="sxs-lookup"><span data-stu-id="03595-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03595-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="03595-117">-Name</span></span>
<span data-ttu-id="03595-118">指定您要取得其部署資訊的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="03595-118">Specifies the name of the website for which you want to get deployment information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03595-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="03595-119">-Profile</span></span>
<span data-ttu-id="03595-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="03595-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03595-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="03595-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03595-122">-槽</span><span class="sxs-lookup"><span data-stu-id="03595-122">-Slot</span></span>
<span data-ttu-id="03595-123">指定槽名稱。</span><span class="sxs-lookup"><span data-stu-id="03595-123">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03595-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03595-124">CommonParameters</span></span>
<span data-ttu-id="03595-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03595-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03595-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03595-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03595-127">輸入</span><span class="sxs-lookup"><span data-stu-id="03595-127">INPUTS</span></span>

## <span data-ttu-id="03595-128">輸出</span><span class="sxs-lookup"><span data-stu-id="03595-128">OUTPUTS</span></span>

## <span data-ttu-id="03595-129">筆記</span><span class="sxs-lookup"><span data-stu-id="03595-129">NOTES</span></span>

## <span data-ttu-id="03595-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="03595-130">RELATED LINKS</span></span>

[<span data-ttu-id="03595-131">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="03595-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


