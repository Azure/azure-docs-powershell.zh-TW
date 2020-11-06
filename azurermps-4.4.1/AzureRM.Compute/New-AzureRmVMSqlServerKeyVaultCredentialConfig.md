---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 922c7e7055c51990b28b472805a68563c94b3e6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456812"
---
# <span data-ttu-id="09c06-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="09c06-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="09c06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09c06-102">SYNOPSIS</span></span>
<span data-ttu-id="09c06-103">針對虛擬機器上的 SQL server 金鑰保存庫認證建立一個 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="09c06-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09c06-104">句法</span><span class="sxs-lookup"><span data-stu-id="09c06-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="09c06-105">說明</span><span class="sxs-lookup"><span data-stu-id="09c06-105">DESCRIPTION</span></span>

## <span data-ttu-id="09c06-106">示例</span><span class="sxs-lookup"><span data-stu-id="09c06-106">EXAMPLES</span></span>

## <span data-ttu-id="09c06-107">參數</span><span class="sxs-lookup"><span data-stu-id="09c06-107">PARAMETERS</span></span>

### <span data-ttu-id="09c06-108">-啟用</span><span class="sxs-lookup"><span data-stu-id="09c06-108">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="09c06-109">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-110">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="09c06-110">-AzureKeyVaultUrl</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-111">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="09c06-111">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-112">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="09c06-112">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="09c06-113">-Profile</span></span>
<span data-ttu-id="09c06-114">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="09c06-114">@{Text=}</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="09c06-115">-InformationAction</span></span>
<span data-ttu-id="09c06-116">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="09c06-116">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09c06-117">-InformationVariable</span></span>
<span data-ttu-id="09c06-118">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="09c06-118">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c06-119">CommonParameters</span></span>
<span data-ttu-id="09c06-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09c06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c06-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09c06-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c06-122">輸入</span><span class="sxs-lookup"><span data-stu-id="09c06-122">INPUTS</span></span>

## <span data-ttu-id="09c06-123">輸出</span><span class="sxs-lookup"><span data-stu-id="09c06-123">OUTPUTS</span></span>

## <span data-ttu-id="09c06-124">筆記</span><span class="sxs-lookup"><span data-stu-id="09c06-124">NOTES</span></span>

## <span data-ttu-id="09c06-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="09c06-125">RELATED LINKS</span></span>

