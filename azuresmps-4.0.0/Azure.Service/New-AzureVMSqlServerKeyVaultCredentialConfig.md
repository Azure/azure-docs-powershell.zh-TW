---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967634"
---
# <span data-ttu-id="ad68d-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="ad68d-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="ad68d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad68d-102">SYNOPSIS</span></span>

## <span data-ttu-id="ad68d-103">句法</span><span class="sxs-lookup"><span data-stu-id="ad68d-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad68d-104">說明</span><span class="sxs-lookup"><span data-stu-id="ad68d-104">DESCRIPTION</span></span>

## <span data-ttu-id="ad68d-105">示例</span><span class="sxs-lookup"><span data-stu-id="ad68d-105">EXAMPLES</span></span>

### <span data-ttu-id="ad68d-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="ad68d-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ad68d-107">參數</span><span class="sxs-lookup"><span data-stu-id="ad68d-107">PARAMETERS</span></span>

### <span data-ttu-id="ad68d-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ad68d-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad68d-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ad68d-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad68d-110">-啟用</span><span class="sxs-lookup"><span data-stu-id="ad68d-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad68d-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ad68d-111">-InformationAction</span></span>
<span data-ttu-id="ad68d-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ad68d-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ad68d-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ad68d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad68d-114">持續</span><span class="sxs-lookup"><span data-stu-id="ad68d-114">Continue</span></span>
- <span data-ttu-id="ad68d-115">理會</span><span class="sxs-lookup"><span data-stu-id="ad68d-115">Ignore</span></span>
- <span data-ttu-id="ad68d-116">看</span><span class="sxs-lookup"><span data-stu-id="ad68d-116">Inquire</span></span>
- <span data-ttu-id="ad68d-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ad68d-117">SilentlyContinue</span></span>
- <span data-ttu-id="ad68d-118">停止</span><span class="sxs-lookup"><span data-stu-id="ad68d-118">Stop</span></span>
- <span data-ttu-id="ad68d-119">封存</span><span class="sxs-lookup"><span data-stu-id="ad68d-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad68d-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ad68d-120">-InformationVariable</span></span>
<span data-ttu-id="ad68d-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ad68d-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad68d-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ad68d-122">-Profile</span></span>
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

### <span data-ttu-id="ad68d-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ad68d-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad68d-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="ad68d-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad68d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad68d-125">CommonParameters</span></span>
<span data-ttu-id="ad68d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad68d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad68d-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad68d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad68d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ad68d-128">INPUTS</span></span>

## <span data-ttu-id="ad68d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ad68d-129">OUTPUTS</span></span>

## <span data-ttu-id="ad68d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ad68d-130">NOTES</span></span>

## <span data-ttu-id="ad68d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad68d-131">RELATED LINKS</span></span>

