---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794924"
---
# <span data-ttu-id="64599-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64599-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="64599-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64599-102">SYNOPSIS</span></span>
<span data-ttu-id="64599-103">停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="64599-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="64599-104">句法</span><span class="sxs-lookup"><span data-stu-id="64599-104">SYNTAX</span></span>

### <span data-ttu-id="64599-105">S1</span><span class="sxs-lookup"><span data-stu-id="64599-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64599-106">S2</span><span class="sxs-lookup"><span data-stu-id="64599-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64599-107">說明</span><span class="sxs-lookup"><span data-stu-id="64599-107">DESCRIPTION</span></span>
<span data-ttu-id="64599-108">**AzWebApp** Cmdlet 會停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="64599-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="64599-109">示例</span><span class="sxs-lookup"><span data-stu-id="64599-109">EXAMPLES</span></span>

### <span data-ttu-id="64599-110">範例1：停止 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="64599-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="64599-111">這個命令會停止屬於名為「預設-Web-WestUS」資源群組的名為 ContosoWebApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="64599-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="64599-112">參數</span><span class="sxs-lookup"><span data-stu-id="64599-112">PARAMETERS</span></span>

### <span data-ttu-id="64599-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64599-113">-DefaultProfile</span></span>
<span data-ttu-id="64599-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64599-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64599-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="64599-115">-Name</span></span>
<span data-ttu-id="64599-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="64599-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64599-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64599-117">-ResourceGroupName</span></span>
<span data-ttu-id="64599-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="64599-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64599-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="64599-119">-WebApp</span></span>
<span data-ttu-id="64599-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="64599-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64599-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64599-121">CommonParameters</span></span>
<span data-ttu-id="64599-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64599-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64599-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64599-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64599-124">輸入</span><span class="sxs-lookup"><span data-stu-id="64599-124">INPUTS</span></span>

### <span data-ttu-id="64599-125">網站地圖</span><span class="sxs-lookup"><span data-stu-id="64599-125">Site</span></span>
<span data-ttu-id="64599-126">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="64599-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="64599-127">輸出</span><span class="sxs-lookup"><span data-stu-id="64599-127">OUTPUTS</span></span>

## <span data-ttu-id="64599-128">筆記</span><span class="sxs-lookup"><span data-stu-id="64599-128">NOTES</span></span>

## <span data-ttu-id="64599-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="64599-129">RELATED LINKS</span></span>

[<span data-ttu-id="64599-130">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64599-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="64599-131">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64599-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="64599-132">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64599-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="64599-133">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64599-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="64599-134">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="64599-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


