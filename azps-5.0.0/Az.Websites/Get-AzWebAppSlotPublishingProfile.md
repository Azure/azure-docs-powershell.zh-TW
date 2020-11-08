---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138572"
---
# <span data-ttu-id="fc0a1-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="fc0a1-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="fc0a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0a1-103">取得 Azure Web App 槽發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc0a1-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="fc0a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc0a1-104">SYNTAX</span></span>

### <span data-ttu-id="fc0a1-105">S1</span><span class="sxs-lookup"><span data-stu-id="fc0a1-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc0a1-106">S2</span><span class="sxs-lookup"><span data-stu-id="fc0a1-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc0a1-107">說明</span><span class="sxs-lookup"><span data-stu-id="fc0a1-107">DESCRIPTION</span></span>
<span data-ttu-id="fc0a1-108">**AzWebAppSlotPublishingProfile** Cmdlet 會取得指定槽的 Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc0a1-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="fc0a1-109">示例</span><span class="sxs-lookup"><span data-stu-id="fc0a1-109">EXAMPLES</span></span>

### <span data-ttu-id="fc0a1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fc0a1-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="fc0a1-111">這個命令會針對與資源群組預設的 web App ContosoWebApp 相關聯的 Slot001，以 Ftp 格式取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="fc0a1-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="fc0a1-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc0a1-112">PARAMETERS</span></span>

### <span data-ttu-id="fc0a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0a1-113">-DefaultProfile</span></span>
<span data-ttu-id="fc0a1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc0a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc0a1-115">-Format</span><span class="sxs-lookup"><span data-stu-id="fc0a1-115">-Format</span></span>
<span data-ttu-id="fc0a1-116">設置</span><span class="sxs-lookup"><span data-stu-id="fc0a1-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0a1-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="fc0a1-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="fc0a1-118">如果 true，則包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="fc0a1-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0a1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc0a1-119">-Name</span></span>
<span data-ttu-id="fc0a1-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="fc0a1-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0a1-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="fc0a1-121">-OutputFile</span></span>
<span data-ttu-id="fc0a1-122">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="fc0a1-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc0a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc0a1-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fc0a1-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0a1-125">-槽</span><span class="sxs-lookup"><span data-stu-id="fc0a1-125">-Slot</span></span>
<span data-ttu-id="fc0a1-126">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="fc0a1-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0a1-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fc0a1-127">-WebApp</span></span>
<span data-ttu-id="fc0a1-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="fc0a1-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0a1-129">CommonParameters</span></span>
<span data-ttu-id="fc0a1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc0a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0a1-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc0a1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0a1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fc0a1-132">INPUTS</span></span>

### <span data-ttu-id="fc0a1-133">System.object</span><span class="sxs-lookup"><span data-stu-id="fc0a1-133">System.String</span></span>

### <span data-ttu-id="fc0a1-134">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="fc0a1-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fc0a1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fc0a1-135">OUTPUTS</span></span>

### <span data-ttu-id="fc0a1-136">System.object</span><span class="sxs-lookup"><span data-stu-id="fc0a1-136">System.String</span></span>

## <span data-ttu-id="fc0a1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fc0a1-137">NOTES</span></span>

## <span data-ttu-id="fc0a1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc0a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="fc0a1-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="fc0a1-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="fc0a1-140">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc0a1-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="fc0a1-141">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fc0a1-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)