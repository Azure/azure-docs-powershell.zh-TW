---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966909"
---
# <span data-ttu-id="ecce3-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="ecce3-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="ecce3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecce3-102">SYNOPSIS</span></span>
<span data-ttu-id="ecce3-103">在 Azure 中 Redeploys 網站的先前部署。</span><span class="sxs-lookup"><span data-stu-id="ecce3-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="ecce3-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecce3-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecce3-105">說明</span><span class="sxs-lookup"><span data-stu-id="ecce3-105">DESCRIPTION</span></span>
<span data-ttu-id="ecce3-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecce3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ecce3-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="ecce3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ecce3-108">**Restore-AzureWebsiteDeployment** Cmdlet 會 redeploys Azure 中先前的網站部署。</span><span class="sxs-lookup"><span data-stu-id="ecce3-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="ecce3-109">這個程式會將目前的部署取代為選取的部署。</span><span class="sxs-lookup"><span data-stu-id="ecce3-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="ecce3-110">示例</span><span class="sxs-lookup"><span data-stu-id="ecce3-110">EXAMPLES</span></span>

### <span data-ttu-id="ecce3-111">範例1：重新部署網站</span><span class="sxs-lookup"><span data-stu-id="ecce3-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="ecce3-112">這個命令 redeploys 具有名為 ContosoSite 之網站之 ID f876543210 的部署。</span><span class="sxs-lookup"><span data-stu-id="ecce3-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="ecce3-113">參數</span><span class="sxs-lookup"><span data-stu-id="ecce3-113">PARAMETERS</span></span>

### <span data-ttu-id="ecce3-114">-CommitId</span><span class="sxs-lookup"><span data-stu-id="ecce3-114">-CommitId</span></span>
<span data-ttu-id="ecce3-115">指定要重新部署之部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ecce3-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="ecce3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ecce3-116">-Force</span></span>
<span data-ttu-id="ecce3-117">如果已啟用，請 redeploys 先前的部署，而不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ecce3-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ecce3-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ecce3-118">-Name</span></span>
<span data-ttu-id="ecce3-119">指定要重新部署的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="ecce3-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="ecce3-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ecce3-120">-Profile</span></span>
<span data-ttu-id="ecce3-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ecce3-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ecce3-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ecce3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ecce3-123">-槽</span><span class="sxs-lookup"><span data-stu-id="ecce3-123">-Slot</span></span>
<span data-ttu-id="ecce3-124">指定槽名稱。</span><span class="sxs-lookup"><span data-stu-id="ecce3-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="ecce3-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ecce3-125">-Confirm</span></span>
<span data-ttu-id="ecce3-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ecce3-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecce3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecce3-127">-WhatIf</span></span>
<span data-ttu-id="ecce3-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ecce3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecce3-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecce3-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecce3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecce3-130">CommonParameters</span></span>
<span data-ttu-id="ecce3-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecce3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecce3-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ecce3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecce3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ecce3-133">INPUTS</span></span>

## <span data-ttu-id="ecce3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ecce3-134">OUTPUTS</span></span>

## <span data-ttu-id="ecce3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ecce3-135">NOTES</span></span>

## <span data-ttu-id="ecce3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecce3-136">RELATED LINKS</span></span>

[<span data-ttu-id="ecce3-137">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ecce3-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ecce3-138">AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="ecce3-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


