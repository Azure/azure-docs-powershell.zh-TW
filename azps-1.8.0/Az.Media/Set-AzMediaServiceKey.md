---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: c80c9b411d360de0b46cd051a3f786bb740b26f2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402349"
---
# <span data-ttu-id="7922c-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="7922c-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="7922c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7922c-102">SYNOPSIS</span></span>
<span data-ttu-id="7922c-103">重新產生用來存取與媒體服務關聯的 REST 端點的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7922c-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="7922c-104">語法</span><span class="sxs-lookup"><span data-stu-id="7922c-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7922c-105">描述</span><span class="sxs-lookup"><span data-stu-id="7922c-105">DESCRIPTION</span></span>
<span data-ttu-id="7922c-106">**Set-AzMediaServiceKey** Cmdlet 會重新產生用於存取媒體服務相關之表示狀態傳輸 (REST) 端點的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7922c-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="7922c-107">例子</span><span class="sxs-lookup"><span data-stu-id="7922c-107">EXAMPLES</span></span>

### <span data-ttu-id="7922c-108">範例 1：重新產生用來存取媒體服務的主鍵</span><span class="sxs-lookup"><span data-stu-id="7922c-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="7922c-109">此命令會重新產生名為 MediaService001 的媒體服務主鍵，該媒體服務屬於名為 ResourceGroup004 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7922c-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="7922c-110">範例 2：重新產生用來存取媒體服務的次要金鑰</span><span class="sxs-lookup"><span data-stu-id="7922c-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="7922c-111">此命令會重新產生媒體服務名為 MediaService002 的次要金鑰，該媒體服務屬於名為 Resourcegroup123 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7922c-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="7922c-112">參數</span><span class="sxs-lookup"><span data-stu-id="7922c-112">PARAMETERS</span></span>

### <span data-ttu-id="7922c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7922c-113">-AccountName</span></span>
<span data-ttu-id="7922c-114">指定此 Cmdlet 重新產生之媒體服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="7922c-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7922c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7922c-115">-DefaultProfile</span></span>
<span data-ttu-id="7922c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7922c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7922c-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="7922c-117">-KeyType</span></span>
<span data-ttu-id="7922c-118">指定媒體服務的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="7922c-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="7922c-119">此參數可接受的值為：主要或次要。</span><span class="sxs-lookup"><span data-stu-id="7922c-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7922c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7922c-120">-ResourceGroupName</span></span>
<span data-ttu-id="7922c-121">指定包含媒體服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7922c-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="7922c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="7922c-122">-Confirm</span></span>
<span data-ttu-id="7922c-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7922c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7922c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7922c-124">-WhatIf</span></span>
<span data-ttu-id="7922c-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7922c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7922c-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7922c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7922c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7922c-127">CommonParameters</span></span>
<span data-ttu-id="7922c-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7922c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7922c-129">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7922c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7922c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7922c-130">INPUTS</span></span>

### <span data-ttu-id="7922c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7922c-131">System.String</span></span>

## <span data-ttu-id="7922c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7922c-132">OUTPUTS</span></span>

### <span data-ttu-id="7922c-133">Microsoft.Azure.Commands.Media.models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="7922c-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="7922c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7922c-134">NOTES</span></span>

## <span data-ttu-id="7922c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7922c-135">RELATED LINKS</span></span>



