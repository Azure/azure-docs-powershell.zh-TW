---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 7b8c1b154a631a911100f4b2b8581ca552e4b565
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454343"
---
# <span data-ttu-id="c7525-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="c7525-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="c7525-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7525-102">SYNOPSIS</span></span>
<span data-ttu-id="c7525-103">重新產生用來存取與媒體服務相關聯之 REST 端點的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7525-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7525-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7525-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7525-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7525-105">DESCRIPTION</span></span>
<span data-ttu-id="c7525-106">**AzureRmMediaServiceKey** Cmdlet 會重新產生一個用來存取 Representational 狀態轉移的金鑰， (與媒體服務相關聯的 REST) 端點。</span><span class="sxs-lookup"><span data-stu-id="c7525-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="c7525-107">示例</span><span class="sxs-lookup"><span data-stu-id="c7525-107">EXAMPLES</span></span>

### <span data-ttu-id="c7525-108">範例1：重新產生用來存取媒體服務的主鍵</span><span class="sxs-lookup"><span data-stu-id="c7525-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="c7525-109">這個命令會重新產生屬於名為 ResourceGroup004 之資源群組之名為 MediaService001 的媒體服務的主機碼。</span><span class="sxs-lookup"><span data-stu-id="c7525-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="c7525-110">範例2：重新產生存取媒體服務時所用的次要金鑰</span><span class="sxs-lookup"><span data-stu-id="c7525-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="c7525-111">這個命令會為屬於名為 Resourcegroup123 之資源群組的名為 MediaService002 的媒體服務重新產生次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7525-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="c7525-112">參數</span><span class="sxs-lookup"><span data-stu-id="c7525-112">PARAMETERS</span></span>

### <span data-ttu-id="c7525-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c7525-113">-AccountName</span></span>
<span data-ttu-id="c7525-114">指定此 Cmdlet 所再生之媒體服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7525-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="c7525-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c7525-115">-KeyType</span></span>
<span data-ttu-id="c7525-116">指定媒體服務的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="c7525-116">Specifies the key type of the media service.</span></span>
<span data-ttu-id="c7525-117">此參數可接受的值為：主要或次要。</span><span class="sxs-lookup"><span data-stu-id="c7525-117">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="c7525-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7525-118">-ResourceGroupName</span></span>
<span data-ttu-id="c7525-119">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7525-119">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="c7525-120">-確認</span><span class="sxs-lookup"><span data-stu-id="c7525-120">-Confirm</span></span>
<span data-ttu-id="c7525-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7525-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7525-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7525-122">-WhatIf</span></span>
<span data-ttu-id="c7525-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7525-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7525-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7525-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7525-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7525-125">-DefaultProfile</span></span>
<span data-ttu-id="c7525-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7525-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7525-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7525-127">CommonParameters</span></span>
<span data-ttu-id="c7525-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7525-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7525-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7525-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7525-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c7525-130">INPUTS</span></span>

## <span data-ttu-id="c7525-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c7525-131">OUTPUTS</span></span>

### <span data-ttu-id="c7525-132">PSServiceKey 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c7525-132">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="c7525-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c7525-133">NOTES</span></span>

## <span data-ttu-id="c7525-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7525-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7525-135">AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="c7525-135">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


